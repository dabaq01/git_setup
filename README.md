# git_setup
i. What you understand by version control?
Version control is basically a system by which developers can track, monitor progress or changes to the files they're working on.

ii. What is the importance of version control.
It fosters team collaboration and allows teams to track the changes members have made to the files over time. It also allows for reverting to earlier versions of the files being worked on in the event of a seemingly insurmountable bug. It also reduces the risk of loss of data.

iii. What is git.
It's a free open source veersion control system which allows for teams to collaborate, manage and track progress of the changes they make to the files they are working on per time.
vi  What is GitHub 
It's an open source distributed systems used particularly for version control as it aids seamless collaboration and efficient project management.

v. Difference between git and GitHub 
While fit is and version control system for tracking and managing source code history, GitHub is a platform for hosting got repositories 

vi. Comprehensive git and GitHub setup for beginners.

First off, it is advisable to search for the terminal commands for installing the "git"on your local computer. The command is; "sudo apt-get install git" because it has to be run by the super user for security reasons. It will run and install the git on your computer.
Secondly, you need to set up your GitHub account if you do not already have one. If you don't, search for the GitHub website and sign up with your email address and create a username and password. After that's done, set up your GitHub profile. You can add your name, photo, social links etc.
After that's done, you have to setup your SSH. 

Identity:
You start by setting your user name and email address. This is very vital as every Git commit uses this information, and it’s immutably embedded into any commits you create.
On your terminal, input the following;
git config --global user.name "your-github-username"
this will set the user name
then input the following;
gitconfig --global user.email "your-email_address"
this will set your email address. you can check the changes using;
git config --list
this should display the username and email you just set up.

SSH Keygen:
Next up, you need to generate your ssh key. To do that, input the following on your terminal;
ssh keygen -t ed25519 -C "your_email_address"
this should generate the key using the probided email as a label. you should keep that key safe. When you're prompted to "Enter a file in which to save the key", you can press Enter to accept the default file location. 
Next you start the ssh agent in the background by inputting the following in your terminal;
eval "$(ssh-agent -s)"
this should generate an agent pid number. you should also keep this safe.
Next you should input the following in your terminal;
ssh-add ~/.ssh/id_ed25519
this will add the ssh key to the private agent
then input the following:
cat ~/.ssh/id_ed25519.pub
then copy the contents to your clipboard.
