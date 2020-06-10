# Git Installation and Setup on Windows

## Installing Git
To download Git:
 1. Go to https://git-scm.com/downloads
 2. Download the software for Windows
 3. Install Git choosing all of the default options

Once everything is installed, you should be able to run git on the command line. If it displays the usage information, then you're good to go!

## Configuring the Command Prompt on Windows

#### First Time Git Configuration
Copy the '.bash_profile' and folder '.git-command-prompt-setup' to your home folder (eg: C:\Users\satish)

Before you can start using Git, you need to configure it. Run each of the following lines on the command line to make sure everything is set up.

**Sets up Git with your name**

git config --global user.name "Your-Full-Name"

**Sets up Git with your email**

git config --global user.email "your-email-address"

**Makes sure that Git output is colored**

git config --global color.ui auto

**Displays the original state in a conflict**

git config --global merge.conflictstyle diff3

git config --list


#### Git & Code Editor
The last step of configuration is to get Git working with your code editor. Below are three of the most popular code editors. If you use a different editor, then do a quick search on Google for "associate X text editor with Git" (replace the X with the name of your code editor).


**Atom Editor Setup**

git config --global core.editor "atom --wait"

**Sublime Text Setup**

git config --global core.editor "'C:/Program Files/Sublime Text 3/sublime_text.exe' -n -w"

**VSCode Setup**

git config --global core.editor "code --wait"
