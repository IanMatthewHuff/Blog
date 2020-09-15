## Getting started with Processing.py and Visual Studio Code

Quick guide here to getting started with Processing.py and how to set it up for usage with Visual Studio Code.

### Installation

For the first step, go to the processing webpage and download it for your platform.

[Processing Download](https://processing.org/download/)

Thankfully it's a simple zip extract. Nothing special to install and muck up your system with. After installing the first thing that I did was go to Tools->Add Tool menu to add in Python mode.

![Python Mode Install](https://raw.githubusercontent.com/IanMatthewHuff/Blog/master/Processing1/Images/PythonModeInstall.PNG)

After that install a quick "hello ellipse" test to make sure that everything was working.

![Basic Working](https://raw.githubusercontent.com/IanMatthewHuff/Blog/master/Processing1/Images/EllipseTest.PNG)

### Processing on the command line

To move away from using the Processing IDE that is bundled with Processing (PDE) and to using VS Code I'm starting with the instructions here:

[Processing Command Line](https://py.processing.org/tutorials/command-line/)

The sad part of this process is that it involves installing Java on my system. Especially given that the first step in this seems to involving installing a specific JRE from Oracle and the first step in getting that is signing up for an Oracle account, which is honestly rather **unbelievable** in this day and age. With a bit of poking around I was able to find a site that allowed me to download the file directly by bypassing the Oracle login.

[Java 8 Direct Download](https://sites.google.com/view/java-se-download-url-converter)

Command line instructions all seem to go pretty smoothly, I did notice that before just creating my own test app I tried to run one of the existing samples and it didn't run properly (Basics\Color\WaveGradient.py) so I plan to go back to check that out as time allows.

![Command Line Working](https://raw.githubusercontent.com/IanMatthewHuff/Blog/master/Processing1/Images/MouseFollowCommandLine.png)
