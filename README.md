# CMPUT 302 Project 1 Deliverable 2

This is the latex document for our 2nd deliverable in the course. Below I outline a procedure for installing LaTeX and setting up the development environment.

The principle file for this document is `report.tex` and the media file is `media`, which will contain all images necessary for the report. All modifications in terms of content should happen in this file.

## Installing LaTeX

I recommend the following software stack for LaTeX workflow:
- TexLive
- TexStudio

I will outline my installation instructions for Linux, I believe this procedure is the same on mac (roughly), for windows I will do my best to point towards documentation and useful sites for troubleshooting.

### TexStudio

This will become your LaTeX 'IDE'. If you want to write in VS Code (or emacs, like me) then that can be configured. I will detail command line compilation of latex documents later. 

#### Linux

On Linux, the installation is pretty darn simple:
`sudo apt-get update && sudo apt-get install texstudio`

This will provide a default installation which I have found works relatively well.

#### MAC

For MAC, I take the instructions from the [TexStudio Website](https://www.texstudio.org/) (**NOTE**: I assume MACOS 11.7 or higher):

1. You need to [download the executable](https://github.com/texstudio-org/texstudio/releases/download/4.7.2/texstudio-4.7.2-osx.dmg)
2. Run and enjoy

This will provide the application in a .dmg file, so you will need to do whatever fancy mac stuff needs to be done to make that run.

#### Windows

This is pretty simple too:

1. [Download the installer](https://github.com/texstudio-org/texstudio/releases/download/4.7.2/texstudio-4.7.2-win-qt6.exe)
2. Run and follow the prompts

### Installing TexLive

The instructions are detailed on the [TexLive website](https://tug.org/texlive/quickinstall.html), I recommend using the [install profile](texlive.profile) that I use, however it is a linux only image so it will not work on mac nor windows.

#### MAC/Linux

The installation takes place through the normal commands. See the website to run them

#### Windows

1. [Download](https://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe)
2. Execute the newly-downloaded install-tl-windows.exe.
3. Change settings as desired and install.
4. Additional Windows-specific info. 


## Setting up the development environment

### TexStudio

You will need to add to the path variable of texstudio to compile with TexLive. To do this:
1. Open TexStudio
2. Options -> Configure TexStudio
3. Enable the **Show Advanced Options** Tickbox (bottom left)
4. Navigate to the **Build** Tab
5. Add the path of the TexLive installation to the $PATH of texStudio (Down at the bottom of the screen)

### Shell/Terminal/Powershell

The compilation command is `pdflatex -synctex=1 -interaction=nonstopmode $FILENAME` (replace `$FILENAME` as required). You may need to perform extra setup to get this to work on windows, I know I had a pain doing it (hence why I use linux now)

A good way to see if TexLive is functional on your system is to try to compile the [DND LaTeX](https://github.com/rpgtex/DND-5e-LaTeX-Template) template on your desired environment. This is more of a LaTeX stress test than a utility, but it ensures that your entire system is up to date.


