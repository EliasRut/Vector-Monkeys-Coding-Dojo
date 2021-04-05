#  Workspace Setup
To make starting out with programming easier, we encourage a somewhat unified workspace setup.
That's not to say that there is a "right" way of how that should look like, individualism is very
much welcome. But for teaching purposes, being able to say "click on that menu, it will bring up
what you need" is really nice. Therefore, there is a recommended starting setup. Feel free to divert
on any point, but be aware that it might make following the lessons harder.

## Recommended starting setup
Our starting setup consists of the following pieces of software. We're providing a short explanation
as to why we are choosing these specific technologies in each of the subpoints.

### Some Linux console
Whenever possible, we recommend that people get used to Linux and command lines early on, since most
servers they will ever interact with are probably running Linux. There are two easy ways of doing
so:

* Directly running a Linux distro (pick your poison, Ubuntu is popular for beginners)
* Running Linux over the Windows Subsystem Linux (requires Windows 10)

### Git as source code management tool
We feel that Git is a good starting point for the world of source code management, and while many
graphical tools exist and many of them will cover everything you need on a day-to-day basis, having
a bit of experience with the command line tool can help a lot in understanding what the whole
process actually does, and to fix more complicated issues. Therefore, we will start out using git
just via the linux command line.

### Node.js, npm
Much of our course is focused on JavaScript. Node.js is by far the most mature and stable engine
for running JavaScript on a server, so we'll make use of it. While there are quite a few good
alternatives to npm, it installs right next to Node.js and is mostly still considered the "default"
package manager - so at the very least, we'll learn the basics of how to use it.

### Visual Studio Code
This might be a more contested choice, especially since there are many great alternatives. Our
criteria ended up being:

* Free to use
* Easy to set up
* Good IDE experience (syntax highlighting, smart suggestions, plugins etc)
* Good integration with Linux on a Windows machine

Visual Studio Code fits the bill well ¯\\\_(ツ)\_/¯

## Step by Step guide
For now we only have guides for Windows 10, MacOs and Linux (Ubuntu to be precise). If you are running
a different Windows version, please let us know.

The instructions start with Mac since it's most different, and the Windows and Linux parts share most
of the setup steps. If you are using Mac, please only do the steps highlighted in __For Mac__.

If you are installing on Windows, please do everything listed under __For Windows__
and under __For Windows and Linux__ - there are multiple such sections.

If you are using Linux, please do everything listed under __For Linux__ and under __For Windows and Linux__.

### For Mac
We will be using the Xcode Command Line Tools for installing the above mentioned software. On Mavericks (10.9) 
or above, you should be able to install what you need by trying to run it from the Terminal the very first time.

#### Nodejs + npm
Open the Terminal by pressing Command+Space to open Spotlight Search and entering Terminal then pressing Enter.
In the Terminal window that appears, write
```
node -v
```
and press Enter.

You can verify that everything works as it should by writing
```
node -v
```
and
```
npm -v
```
which should both give you back a version listing as response.

#### git
Open the Terminal by pressing Command+Space to open Spotlight Search and entering Terminal then pressing Enter.
In the Terminal window that appears, write
```
$ git --version
```
and press Enter. Again, you should get a version listing as response once git is installed.

#### Visual Studio Code
You should be able to just download Visual Studio Code under the link here:
[Link to visual studio code website](https://code.visualstudio.com/download)

### For Windows
Before we can use a Linux distribution on Windows, we have to activate the Windows subsytem for Linux. 
There are 2 easy ways to do so.

* Open a Windows powershell as administrator an run the command:
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
* Search Windows Cortana for "Windows feature on and off" scroll all the way down until you find 
"Windows-Subsystem for Linux", activate the checkbox and Save your changes.

Which ever way you choose, a system restart will be required.

Once that's done you can go ahead and download and install your favorite Linux distribution.

### For both Windows and Linux
#### Nodejs + npm
First, we'll make sure that you don't currently have Node.js installed, by running the uninstall
steps. For that, we will run the package managers removal method on both nodejs and npm, as 
administrator. The full command for Ubuntu (18.04) looks like this:
```
sudo apt remove nodejs npm
```
__Explanation:__
* sudo will run the next provided command with administrator (root) privileges.
* apt is the "Advanced Package Tool" which handles the installation and removal of software on many
Linux distros.
	* remove is the apt parameter for deleting a package of software
	* we finishe the command with a list of software packages we want to deinstall, in our case that is
		* nodejs and
		* npm

When you've understood what will happen once you execute the command above, go ahead and do so.

When that is done, we will install nvm - Node.js version manager.
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash
```
__Explanation:__
* curl is a powerful Linux commandline tool to access web content
* bash - is used to execute the bash code we downloaded from the website. bash is it's own
programming language, and it's one that most linux distros come with preinstalled.
	* So basically, we download code via curl, and via the pipe operator, execute what we downloaded
with the bash command, as administrator thanks to sudo.
		* This is an incredibly unsafe, but pretty common, practice.

At this point, all we have done is install nvm, but not yet Node.js and npm itself. But to use nvm, you will need to restart your WSL terminal once.

After the restart, you can verify nvm is installed by typing

```
nvm --version
```

this should print some version number. You can then install the current version of Node.js and npm by executing:

```
nvm install node
```


Once this has finished, you should be able to verify that the installation was successful by running
```
node -v
```

and 
```
npm -v
```

both should give you some version numbers back.

#### Git
To install git on your Linux console, simply use apt.

```
sudo apt install git
```

To verify this worked as intended, you can run

```
git --version
```
which should again show some kind of version number.

### Only for Windows
As a final step, go and install Visual Studio Code on your Windows environment - not your Linux
machine. Careful, Visual Studio Code is not the same as Visual Studio.

This should also automatically install the server parts into your WSL environment, so that we can
run Visual Studio Code from there.

### Only for Linux
If your base operating system is Linux, go on and install Visual Studio Code directly onto Linux.

### For both Windows and Linux
You should now go and verify that your Visual Studio Code setup is working as intended. For that,
open a new Linux console and execute
```
code .
```
__Explanation:__
* code is the command to start Visual Studio Code
* . always refers to the current directory, ergo the directory your console has currently open. The
code command takes a directory to be used as workspace as it's first parameter


This should open a new Visual Studio Code instance, with your Linux home folder as the current
working directory.

## Create a GitHub Account
If you don't have one yet, please set up a GitHub Account. We'll use it all out through the course
to get experience with Git.
