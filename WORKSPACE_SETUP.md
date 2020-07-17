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

Visual Studio Code fits the bill well ¯\_(ツ)_/¯

## Step by Step guide
For now we only have guides for Windows and Linux (Ubuntu to be precise). If you want to help out
with a Mac guide, please let me know.

### For Windows
The Windows setup needs a few additional steps prior to the shared setup steps, these will deal with
setting up WSL.


### For both Windows and Linux
#### Nodejs + npm
First, we'll make sure that you don't currently have Node.js installed, by running the uninstall
steps. For that, we will run the package managers removal method on both nodejs and npm, as 
administrator. The full command for Ubuntu (18.04) looks like this:
```
sudo apt remove nodejs npm
```
* sudo will run the next provided command with administrator (root) privileges.
* apt is the "Advanced Package Tool" which handles the installation and removal of software on many
Linux distros.
	* remove is the apt parameter for deleting a package of software
	* we finishe the command with a list of software packages we want to deinstall, in our case that is
		* nodejs and
		* npm

When you've understood what will happen once you execute the command above, go ahead and do so.

When that is done, we will setup the installation of a new version of nodejs directly from the
distributors website. The command for that looks like this:
```
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
```
* curl is a powerful Linux commandline tool to access web content
	* -sL are parameters that change the way curl behaves. -sL is short form for -s -L
		* -s stands for silent, so no download progress will be displayed
		* -L is used to follow HTTP redirects instead of stopping the request, e.g. when a page moved.
	* https://deb.nodesource.com/setup_10.x is the url we want to pull the node setup script from.
		* If you want to use a different version than 10.x, specify it here. e.g. setup_12.x
	* | is called a pipe, it takes the input from the previous command and forwards it to the next one.
	* sudo we already talked about
		* -E is a parameter for sudo, which informs sudo that we want to keep the current environmental
variables although we'll run the following command with administrator privileges
	* bash - is used to execute the bash code we downloaded from the website. bash is it's own
programming language, and it's one that most linux distros come with preinstalled.
		* So basically, we download code via curl, and via the pipe operator, execute what we downloaded
with the bash command, as administrator thanks to sudo.
			* This is an incredibly unsafe, but pretty common, practice.

At this point, all we have done is prepare apt for installing the correct version of nodejs. The
installation itself can now be done by running:

```
sudo apt install nodejs
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

#### Create a GitHub Account
If you don't have one yet, please set up a GitHub Account. We'll use it all out through the course
to get experience with Git.

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
* code is the command to start Visual Studio Code
* . always refers to the current directory, ergo the directory your console has currently open. The
code command takes a directory to be used as workspace as it's first parameter


This should open a new Visual Studio Code instance, with your Linux home folder as the current
working directory.

