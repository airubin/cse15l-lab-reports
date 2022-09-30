# Lab Report - *Week 1*
## Logging into your Course-Specific Account 
### *September 30, 2022*
&nbsp;

## **I. Installing VS Code**
The first step you need to take is installing an IDE called VS Code. 
1. You can download VS Code [here.](https://code.visualstudio.com/download)
![Image](VSCodeDownload.png)
2. Once it's done downloading, find it in your downloads folder, and double click to open.
![Image](VSCodePackage.png)
3. Follow the on screen directions to install on your computer!
&nbsp;

## **II. Remotely Connecting**
Now that we have VS Code installed, we can use it to remotely connect to the university's computers.
1. In the menu bar of VS Code there is an option called 'Terminal', click this, then open a new terminal
![Image](TerminalWindow.png)
2. In the terminal, type `ssh cs15lfa22__@ieng6.ucsd.edu`
3. You should then be prompted to enter your ETS password *(Note: when typing, there is no feedback, it will look like you are not typing anything)*
4. Hit enter, and after a second, a message will appear confirming that you have successfully connected!
![Image](LoggingInSSH.png)
&nbsp;

## **III. Trying Some Commands**
Yay! We're in! Now to actually run some commands.
1. To explore the file system of the remote connection, there's a couple commands we can use.

+ `cd ~` to change the directory to the home directory
+ `ls` to list the files in the current directory
+ `cat <file>` to output the contents of a given file
+ `pwd` to print where in the directory you are
![Image](Commands.png)
&nbsp;

## **IV. Moving files with `scp`**
Okay, so now you have some files on YOUR computer that you want to use on the remote one. How can we do this? With `scp`! This command lets us copy files from our local directory to the remote one. Here's how to do it!
1. Either create or locate the file you want on the remote 
&nbsp;

## **V. Setting an SSH Key**

&nbsp;

## **VI. Optimizing Remote Running**

&nbsp;
