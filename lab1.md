# **Lab Report 1: Remote Access and FileSystem**
## *The following report will provide instructions to log into a course-specific account.*

## **STEP 1: Installing VScode**
My computer already has Visual Studio installed, but to start, click on this hyperlink to the [Visual Studio Code website](https://code.visualstudio.com/). Download the version of VSCode that matches the operating system your device uses. Follow the instructions given depending on your device.
![Image](vscodeSite.jpg)

After opening the application, your screen should look like this. Keep in mind that the appearance (colors, menu bar) may differ based on your device and settings. 
![Image](vscode.jpg)

## **STEP 2: Remote Connection**
Now, you can establish the remote connection using terminal on Visual Studio Code. Open a new terminal on VSCode. At the prompt that appears on terminal paste the following command after replacing the "xx" with the two letters at the end of your course specific account username (keep in mind that the "$" dollar sign does should not be included in the command you input):
'''
$ ssh cs15lwi23xx@ieng6.ucsd.edu
'''
At the prompt, enter the password for your account. At that point, you should see the following screen:
![Image](remoteConnection.jpg)

## **STEP 3: Attempting Commands**
At this point, try a few commands! Some popular ones include:
'''
$ cd ~ 
$ cd
$ ls
$ pwd
$ mkdir
$ cp
$ cat
'''
The following screenshot shows me create a .txt file in my account's folder and performing some commands on it. 
![Image](commands.jpg)
