## Hello Flutter

I've always had an interest in UI frameworks, so I wanted to give Flutter a quick look see. I plan on making a few posts following along with the process of getting it up and started as well as some early development work.

### Installing

[Windows Installation](https://flutter.dev/docs/get-started/install/windows)

To start with, the installation consisting of just unzipping to a directory and adding to that path was much appreciated. Years of working with Visual Studio have given me too much fear every time I install a dev tool on my machine. Will I be able to remove it? What is it actually installing? Love knowing that I can just delete a folder and clear it from my path to get back to zero Flutter on my box. The `flutter doctor` application was also very helpful to provide a quick command line look at exactly what I had installed on my system and if I was ready to run.

![Flutter doctor](https://github.com/IanMatthewHuff/Blog/blob/9a31e404f7befd89a9c27db53a6fb6dc456685aa/HelloFlutter1/Images/FlutterDoctor.PNG)

### VS Code Setup

VS Code is my editor of choice (full disclosure, I work on the Microsoft Python Extension for VS Code) so I appreciated having editor specific steps to get things set up for it.

[VS Code Editor Setup](https://flutter.dev/docs/get-started/editor?tab=vscode)

The integration seems good here so far. I like that the effort was taken to enforce even on the smaller conventions, like the new project command making sure to validate that Flutter naming conventions were being followed before creating.

[Flutter naming warning](https://github.com/IanMatthewHuff/Blog/blob/2b2b3503ed2c71e13ecf456b4ee05d11d90c7edf/HelloFlutter1/Images/NameWarning.PNG)

### Android SDK / Emulator setup

In a previous career step at Microsoft I used to maintain the Visual Studio C++ tooling for cross-platform mobile development. At the stage that it was at the product was pretty well in place, so much of the work involved was around getting the correct SDKs and emulators installed to keep up with Android releases. It was quite a hassle at times, and my take away from this was that I wanted to rely on Google handling as much as possible. So to get the SDKs and an emulator installed I went with installing Android Studio and using the SDK and AVD manager with that to get things installed.

### Hello Flutter
