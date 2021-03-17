## ArtBook creating a notebook interface for Processing.py sketches in VS Code

In my day job for the VS Code Jupyter extension I've been working some with the new Notebook API that VS Code has created. I love working with the team, but I wanted a chance to explore the API a bit on my own. So my goal here is to combine digital art (with Processing.py) with the VS Code notebook interface.

### Starting out

To start things out I'm working with the VS Code [helloworld-test-sample](https://github.com/microsoft/vscode-extension-samples/tree/main/helloworld-test-sample) project. This project gives me the basic skeleton for a new extension as well as a basic test for the extension.

For the work that I'm doing I'll be using the [VS Code Notebook API](https://code.visualstudio.com/api/extension-guides/notebook) as my main reference point.

### NotebookContentProvider

The first bit that I'm going to implement is the NotebookContentProvider. This provider is in charge of the connection between the cells in the notebook document at the actual document saved on disk.

One thing to note here, the notebook API is currently in proposed state, so you should add "enableProposedApi": "true" to the package.json of your extension. And also make sure that you're using a vscode engine version that supports it and update your vscode types in the devDependencies if needed.

More info on [Proposed API here](https://code.visualstudio.com/api/advanced-topics/using-proposed-api).

When in Proposed API things can change quickly. So sometimes sample will get out of date, and it's best to refer to the vscode.proposed.d.ts for the main source of truth. Even with just the basic sample from the notebook API page CellKind needs to be updated to NotebookCellKind. Along with a few other changes.

At this point I had enough to run and compile on, so I created a quick little JSON file format based on the sample and debugged the extension. Stuck a quick BP in the content provider load function to make sure that I was hitting the right spot.

![Debugging ContentProvider](https://raw.githubusercontent.com/IanMatthewHuff/Blog/master/ArtBook1/Images/contentProviderBP.PNG)
![File Open](https://raw.githubusercontent.com/IanMatthewHuff/Blog/master/ArtBook1/Images/notebookOpen.PNG)

Note that the notebook API does lots of stuff for me already. Markdown cells show markdown content, and since I set the cell language as Python in the content provider each code cell is basically a small instance of the VS Code editor with a Python file.

### NotebookKernel

At this point we have quite a bit more to do with the ContentProvider, but let's park that for a minute to get to the execution side of things. And for that we're going to need a [NotebookKernel](https://code.visualstudio.com/api/extension-guides/notebook#kernel).

While the ContentProvider provides the visualization and loading / saving of the file the NotebookKernel is what is needed to actually execute cells in the notebook and return output.

Since the ContentProvider and NotebookKernel are disassociated at this point we need to link the two together. To do this we'll use a NotebookKernelProvider. In more complex cases it can be beneficial to separate these out more. One extension could provide the visualization for a notebook document, while multiple other extensions could provide different implementations for backing kernels. The user can just pick between them using the notebook kernel picker in the bottom right of notebook files. But for my work here I just want a 1:1 mapping so it's just a simple case of mapping my viewType 'art-book' with my NotebookKernel class. The viewType here is the one registered in the notebookProvider of package.json. It's used as an id for editors with this type of document open in a number of places, such as activation events and "when" clauses for contributed commands.

At this point when we debug now and hit the run button on a code cell we can see that the executeCell function in our ArtBookKernel is getting hit.

![Kernel BP Hit](https://raw.githubusercontent.com/IanMatthewHuff/Blog/master/ArtBook1/Images/notebookKernelBP.PNG)
