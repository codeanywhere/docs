---
title: Codeanywhere Documentation

toc_footers:
  - <a href='https://codeanywhere.com'>Back to Codeanywhere</a>

includes:

search: true
---

# Getting started

## Welcome
Welcome to the official Codeanywhere documentation! Here you'll find articles and tutorials to help you get started with the Codeanywhere platform. These include everything from setting up your editor, to learning how to deploy your code! See something that's not documented here? Send an e-mail to [support@codeanywhere.com](support@codeanywhere.com) and we'll get it in.

### Getting More Help
If you need any assistance, feel free to contact us and we will help you as soon as possible! There are several ways for you to contact us:

1. Send in your request to [support@codeanywhere.com](support@codeanywhere.com)
2. Inside your Editor, go to Help -> Create a Support Ticket
3. Submit a feature request inside your Editor, at Help -> Suggest a Feature
4. Chat - contact us directly from codeanywhere.com by sending us a message in your bottom left corner. Don't forget to type in your e-mail so you can receive our response. 
5. Feel free to add us on [Twitter](https://twitter.com/codeanywhere) or [Facebook](https://www.facebook.com/Codeanywhere/)!

### Recent updates
All of our updates, fixes, and improvements are shown inside your Editor in the Config Log (Help -> Change Log), feel free to browse them and find out what is new in Codeanywhere! Also, please follow our [Website](https://codeanywhere.com) and [Blog](https://blog.codeanywhere.com/) for news on updates and upgrades!

## What is Codeanywhere?

Codeanywhere is a Cross Platform Cloud IDE and it has all the features of Desktop IDE but with additional features only a cloud application can give you! Codeanywhere is very flexible and you can set up your workflow any way you want it. The elegant development environment will let you focus on building great applications quicker. All the features you will need for any coding task are built into Codeanywhere, making development more productive and fun. Codeanywhere can edit many types of files and has all the nice features you are used to in desktop editors:

* More than 120 Programming languages syntax
* Code completion (js, php, html, css)
* Linting (js, css)
* Multiple cursors
* Zen coding support
* Code beautify
* All device and browser support
* Drag and Drop files and folders from your Desktop and edit them
* Open and save files with more than 200.000 lines

Codeanywhere has integrated clients for connecting to FTP, SFTP, FTPS, SSH, Dropbox, Amazon S3, Google Drive, GitHub, Bitbucket and even DigitalOcean, so you can code and deploy without opening up multiple programs! Also, you can create Containers which are your private virtual development environment that you can fully customize through SSH terminal. Each one comes with its own dedicated amount of memory and disk space. You can choose between a large number of predefined stacks (PHP, HTML, Laravel, Wordpress, etc.) or you can create new ones! You can preview your application instantly inside Codeanywhere IDE. Our large file support enables you to open and save files with over 200.000 lines! You can even drag and drop files and folders from your Desktop! Codeanywhere has a sharing capability so you can get help from a colleague, open your code base to a group or simply to show your latest code to your friends and Revisions so you don't have to worry about losing your code ever again!

In short, Codeanywhere will solve all your coding needs on the go, anytime, anywhere and on any platform!


## Quick Tutorial

### Registration and Login

To get started with Codeanywhere, just [Register](https://codeanywhere.com/register) with an account or [Login](https://codeanywhere.com/login) if you are already registered and go to our [Editor](https://codeanywhere.com/editor)!

![](http://docs.codeanywhere.com/images/signup.png)

### Starting up

For this tutorial, we’ll show you how to work with our [Containers](#container), although, you can set up your [SSH](#sftp-ssh)/[FTP](#ftp) server right away, or connect to [Google Drive](#google-drive), [Dropbox](#dropbox), [Amazon S3](#amazon-s3), and even import your existing [repository](#git-from-url) or create your [DigitalOcean Droplet](#digitalocean)! Containers are in essence your own Virtual Private Servers which run invisibly in the background of Codeanywhere, each one with its own amount of RAM, Disk space and Processing power. Containers give you the ability to provision any Development Environment you like. You can even choose between one of the predefined stacks.

In order to start a new [Container](#container), go to File -> New Connections -> Container.

![](http://docs.codeanywhere.com/images/tutorial1.png)

Now, you can choose which predefined stack you’d use. In this tutorial, we’ll create a simple PHP container. Choose which OS you’d like to use - Ubuntu or CentOS - and decide whether you’d like for your Container to be Always on - meaning it will be turned on even when you’re offline.

![](http://docs.codeanywhere.com/images/container-php.png)

Wait for a few seconds until your Container is deployed, and you can start coding right away.

![](http://docs.codeanywhere.com/images/container-created.png)

With a right click on your Container, choose to Create a File, and name it “index.php”.

![](http://docs.codeanywhere.com/images/createfile.png)

You can see in your file tree that your Container is already updated! Go to your file and enter some code - in this example we created a simple “Hello World” app.

![](http://docs.codeanywhere.com/images/indexphp.png)

Save it (just like anywhere else with CMD + S, for Mac, or Ctrl + S, for Windows), and now, all you have to do is select “Run” button with a right click on your app:

![](http://docs.codeanywhere.com/images/run.png)

and you’ll be able to preview your new app!

![](http://docs.codeanywhere.com/images/container-run.png)

That’s about it!

You can now [share](#share) your code or work with your colleagues in the same way you’d do that with Google Docs with our [collaboration feature](#pair-programming), and even [share your terminal](#ssh-realtime-collaboration)! If they make some changes you’re not happy with, use our [Revisions feature](#revisions), and get your code back to where you’d like! Sounds interesting? Read our online documentation and learn more about the rest of the cool features we have to offer! :)




## FAQ

### How can I preview my code?
You will need to copy your code into a Container. Containers are basically Virtual Machines and you can use them for all your coding. Each one with its own amount of RAM, Disk space and Processing power. Containers give you the ability to provision any Development Environment you like. You can even choose between one of the predefined stacks. Place your code in, right click and select Run and that's it! If you need a quick tutorial for setting this up, check [here](#quick-tutorial). You can also check [here](#container) for more details on Containers!

### How can I use Git with Codeanywhere?
Codeanywhere will create a [Container](#container) for each repository and you will be able to edit your code directly from there. Then, you can push changes back to your repo using your SSH Terminal! Just check our [Working with Repositories](#working-with-repositories) section for further instructions.

### Why is working with FTP slower on Codeanywhere than with the FileZilla?
While working with FileZilla you are directly connected from local computer to your server, on the other hand the Codeanywhere is acting as a "middle man" between user and ftp - any action done by user is firstly processed at our server and then sent to the ftp. Same thing works in opposite direction, ftp sends response to Codeanywhere and then Codeanywhere forwards the response back to user. Also, the speed of the server response depends on the server location. If your server is located it America, the response will be faster, but if it's located in China it will be slower. We do however plan to expand our server coverage around the world for faster connections.

### How can I connect to Local Server?
Codeanywhere uses its file services in the cloud that are used for making connections. Behind the scenes it looks something like this:

Codeanywhere Web or mobile app ---> Codeanywhere API ---> Codeanywhere File Service ---> Your Server

Your server is in your local network and the only way you could connect to your server from Codeanywhere is that you use port forwarding on your router to your local server. The other problem that could come in your case is your router's public IP. If your internet provider does not provide you a static IP, then you would also need to use some of DDNS services.

### Why is my server not responding after I made few requests, but after an hour works fine again?
While performing actions using Codeanywhere, the requests are sent from our app to your server. Sometimes the number of requests cause your server to block the requests and add Codeanywhere to a blacklist. To avoid this you must make sure that your server is reachable from the following IP addresses:

* 65.52.184.164
* 51.141.5.180
* 52.161.27.120
* 54.187.136.143
* 54.187.142.118
* 54.187.182.165
* 54.187.44.75

If you have no administration rights on the server, please ask your administrator to whitelist these IP’s.

### How to connect local machine to a Container via Putty?
Here are the complete instructions for connecting to your container with Putty:

To generate a set of RSA keys with PuTTYgen:

1. Start the PuTTYgen utility, by double-clicking on its .exe file
2. For Type of key to generate, select SSH-2 RSA
3. In the Number of bits in a generated key field, specify either 2048 or 4096 (increasing the bits makes it harder to crack the key by brute-force methods)
4. Click the Generate button
5. Move your mouse pointer around in the blank area of the Key section, below the progress bar (to generate some randomness) until the progress bar is full
6. A private/ public key pair has now been generated
7. In the Key comment field, enter any comment you'd like, to help you identify this key pair, later (e.g. your e-mail address; home; office; etc.) -- the key comment is particularly useful in the event you end up creating more than one key pair
8. Click the Save public key button & choose whatever filename you'd like (some users create a folder in their computer named my_keys)
9. Click the Save private key button & choose whatever filename you'd like (you can save it in the same location as the public key, but it should be a location that only you can access and that you will NOT lose! If you lose your keys and have disabled username/password logins, you will no longer be able log in!)
10. Right-click in the text field labeled Public key for pasting into OpenSSH authorized_keys file and choose Select All
11. Right-click again in the same text field and choose Copy.

Container config:

1. Log on to your container
2. Run: vim ~/.ssh/authorized_keys
3. Paste key in new line
4. Save and exit

Putty config:

1. Start PuTTY by double-clicking its executable file;
2. PuTTY's initial window is the Session Category (navigate PuTTY's various categories, along the left-hand side of the window);
3. In the Host Name field, enter the Container’s Host Name (hostXX.codeanyhost.com)
4. Enter the port number in the Port field (see Container info)
5. Select SSH under Protocol;
6. Along the left-hand side of the window, select the Data sub-category, under Connection;
7. Specify the username cabox in the Auto-login username field;
8. Expand the SSH sub-category, under Connection;
9. Highlight the Auth sub-category and click the Browse button, on the right-hand side of the PuTTY window;
10. Browse your file system and select your previously-created private key;
11. Return to the Session Category and enter a name for this profile in the Saved Sessions field
12. Click the Save button for the Load, Save or Delete a stored session area.
13. Click on the desired connection and then “connect”

### How can I connect to the SSH of my Container (Linux and OSX)?
1. Open your Terminal
2. Type in ssh-keygen and you will create your public key
3. Go to .ssh/id_rsa.pub and copy your entire key
4. In Codeanywhere, in Container's SSH, use command: cat .ssh/id_rsa.pub
5. Use command vim authorized_keys
6. (type "A" or "I") paste your key in new line and Save (by pressing ESC, and entering :wq)
7. Locate SSH port number in Container's Info
8. Now in order to connect to your box, you have to use the following command to create a tunnel from your local machine to your Container:

~~~~
ssh -p port cabox@hostXX.codeanyhost.com -i id_rsa
~~~~

### How to connect local MySQL to a Container?
After connecting to your local machine via Putty or Terminal, connect to your remote MySQL using: localhost:3306

### How can I connect to a Container via FTP?
You can't connect via FTP but you can connect as SFTP. These are the credentials you'll need:

* Hostname: hostname of your container - looks something like hostXX.codeanyhost.com and you can check it in Container's Info with a right click on your Container
* User name: cabox
* As for the password, you can't connect this way. You'll need private key of your Container and you can get it by going to /home/cabox/.ssh/id_rsa and that's your private key which you can use for connecting to your Container.
* Also, you'll need to check your Port - right click on your Container, select Info, locate SSH Terminal listening on port, and that's the port you have to use for connecting to SFTP.

### How can I find private and public key of my Container?
You can view Private Key of your container by going to cd /home/cabox/.ssh/ using your SSH terminal. There you will find:

* id_rsa - private key container of your container,
* id_rsa.pub - public key of your container.

### Is it possible to deploy to Heroku?
Deploying with Heroku requires you to install Heroku toolbelt. You can install it using SSH command:

~~~~
wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh
~~~~

Now you can use Heroku CLI. More detailed instruction can be found on official Heroku toolbelt website [https://toolbelt.heroku.com/](https://toolbelt.heroku.com/)

### Why doesn't my stack work on 127.0.0.1:port?
Some of our stacks will default the IP to the localhost: 127.0.0.1. You have to change the default IP so your Container could run externally. Please change IP address on your container from 127.0.0.1 to 0.0.0.0 so that you could be able to preview your Ruby box. You can do that inside Config - under commands - of your container (right click on your container and select Config).

For example, on Ruby stack, you just have to use the following command in order to run your Rails container: "rails s --binding=0.0.0.0" This will override localhost (127.0.0.1) where your app can't work. And now, you'll be able to view your Ruby app on: containername-username.codeanyapp.com:3000.

### In a Wordpress stack, after uploading plug-ins, I receive an error and permission is denied. Why?
You can prevent these issues by running commands in SSH:

Ubuntu:

~~~~
sudo chown cabox:www-data -R ~/workspace 
~~~~
CentOS:

~~~~
sudo chown cabox:apache -R ~/workspace
~~~~

Also, please download original plug-ins from Wordpress, so you don't receive this error again.

### I receive the following error when trying to access Google Drive: Invalid token. What could cause this?
There seems to be something wrong with your long-term access token, so please try removing and adding your Drive account. If that does not work please try revoking access to Codeanywhere from your Google security page located at: [https://www.google.com/settings/security](https://www.google.com/settings/security) and afterwards try to add it again.

![](https://docs.codeanywhere.com/other/images/google-invalidtoken.png)


### How can I change Preferences? All I get is a JSON file.
In our current version, it is possible to override settings from Preferences -> Default, inside Preferences -> User/Project.

For example, in Preferences -> Default -> General, you'll see it is set to:

~~~~
"workspace": { 
    "theme": "monokai" 
} 
~~~~

And now you can change it inside Preferences -> User/Project -> General, by adding code:


~~~~
"workspace": { 
    "theme": "white" 
} 
~~~~

And by doing this, you'll override settings from Default. We'll keep updating this so stick around!

### How can I connect to Bitbucket via authorized_keys?
The recommended method is adding Codeanywhere SSH key to your Bitbucket account. That way, you can push commits to your private repo without password prompt. To do so, copy your Codeanywhere public key (you can find it by clicking your email in editor, then click "get your public key") and paste it to your bitbucket account (Account -> manage account -> SSH keys -> add Key)

Now your Codeanywhere account is authorized to make changes to your repo.

If you already have repository in Bitbucket, just by cloning your repository, your git will be setup. If you have existing project with empty Bitbucket git repository, you can add your repo with "git remote add origin {GIT_SSH_URL}". You can find your {GIT_SSH_URL} by clicking clone in bitbucket repo, then copying url next to 'git clone', its format is git@bitbucket.org:/username/repository.git

Now you have successfully setup your git.

### I can't see organizations repositories. How can I setup this?
You have to explicitly allow Codeanywhere to access your organizations. You can do it in two ways:

1. During authorization process Click Grant / Request Access on organization which repositories you want to access through Codeanywhere
![](https://docs.codeanywhere.com/other/images/pic1.png)

2. While logged in your GitHub account, click Account -> Settings -> Applications -> Codeanywhere Click Grant / Request Access on organization which repositories you want to access through Codeanywhere
![](https://docs.codeanywhere.com/other/images/pic2.png)

After allowing organization access, you can list your repositories through Codeanywhere.

### How can I work with my repository with Codeanywhere
Connect to your repository via [Github](#github) or [Bitbucket](#bitbucket) directly or with [Git From URL](#git-from-url). You can push changes to your repository using standard git commands inside your SSH terminal:

`git add -A // To track all files`

`git commit -am "message" // To commit changes`

`git push origin master // Push your local changes to repository`


# Codeanywhere Overview
## Register/Login
To get started with Codeanywhere, just Register with an account or Login if you are already registered and go to our Editor!

### Register
You can Register with Codeanywhere by selecting Sign Up on our Home page.

![](https://docs.codeanywhere.com/overview/images/signup.png)

Now you can choose between multiple registration methods:

Entering your e-mail and password which will be used upon your future sign in
* Using your Google Account
* Using your Bitbucket account
* Using your GitHub account
* Using your Facebook account

In case you choose any of the oAuth methods, you'll have to authorize Codeanywhere for it to be able to access it again.

### Login
You can log into your account if you already have an account. Simply choose between the method you used for registration and you'll be redirected to your Editor!

![](https://docs.codeanywhere.com/overview/images/signin.png)

### Forgot Password
If you forget your password, want to set an password for any of the oAuth methods, or have any problems while logging in to Codeanywhere you can use "Forgot password?" link to reset your password. It is located below login form:

![](https://docs.codeanywhere.com/overview/images/signin-forgotpassword.png)

Once you receive email for your password reset, follow the link and enter the new password. After that you can use the new password and your email to login to your Codeanywhere account.

## Codeanywhere UI
Codeanywhere contains features you'd expect from traditional desktop editors. Among these include:

* Save file option
* Undo and Redo support
* Cut, Copy, Paste, and Replace functionality
* Line manipulation, including:
  * Indenting and outdenting
  * Moving and copying lines up or down
  * Removing lines from any point
  * Splitting lines
* Highlighting and commenting blocks of code
* Revisions
* Code folding (including the entire file)
* Converting cases
* Autocompletion
* Code analysis
* Search in files with regular expressions
* Line wrapping, to a defined column or the width of the browser window
* Support for spaces and real tabs

Codeanywhere can be thought of as being divided into the following components:

1. The top menu bar is the uppermost area, with easy access to a variety of menus
2. The file explorer on the left lets you manipulate various aspects of your project, including its active files, preferences, and choices for deployment. It also displays views according to what's been selected in the file explorer
3. The editor is the main area where you write your code
4. Terminal allows you to SSH directly from your browser
5. The status bar is the bottom area of the window. It shows all sorts of information about your code

![](https://docs.codeanywhere.com/overview/images/editor.png)

### The Top Menu Bar
In this section, you can find the usual menus for creating, opening and saving files, changing your view, and switching between windows.

![](https://docs.codeanywhere.com/overview/codeanywhereui/images/topmenubar.png)
Under the "Help" menu, there is a Change log button which will direct you to all the recent changes, link to our Documentation, Send Feedback button where you can send your comments and feedbacks about Codeanywhere, as well as link to our Terms of Service and Privacy Policy.

Notifications will show you all the changes made – once you create new file, share a file, or upload one, ect. On the far right you can see a Profile button.

![](https://docs.codeanywhere.com/overview/codeanywhereui/images/dashboard-access.png)

It allows you to go to your [Dashboard](#dashboard) - where you can view your subscriptions, projects and shares, change your password or delete your account - or to log off from the Editor, returning you to the Codeanywhere [homepage](https://codeanywhere.com).

### File Explorer
The File Explorer is located on the left side of the Codeanywhere Editor. Inside of the File Explorer you can find all the connections you've made with files and folders linked with them within one Project. With a right click on your Project you'll can choose if you'd like to switch an Project, share your entire Project with other users, add a new one, manage existing ones (this will redirect you to your Dashboard), add new connection within a Project, or just refresh your current Project.

![](https://docs.codeanywhere.com/overview/codeanywhereui/images/project.png)

Each of the connections you can make is explained below:

* Container - your own Virtual Private Servers with its own amount of RAM, Disk space and Processing power – * contains a list of folders and files within your Container
* GitHub – a container with your GitHub repository
* Bitbucket – container with your Bitbucket repository
* Git from URL - container with your repository
* FTP – contains a FTP/FTPS servers
* SSH – contains a SSH/SFTP servers
* Google Drive – shows the list of folders and files on your Google Drive account
* Dropbox – shows the list of folders and files on your Dropbox account
* Amazon S3 – shows the list of folders and files on your S3 account
* DigitalOcean - a Droplet from DigitalOcean

Clicking on any connection or folder expands its menu. Clicking on an expanded button causes it to collapse, which gives you more room in the File Explorer to work with.

Right-click on any file/folder in File Explorer opens a drop-down menu that provides a list of options that can be performed. For a container, you can choose whether you'd like to run it, edit Config file, ect.

### The Code Editor
### Terminal
### Status Bar

## Dashboard
## Projects

# Connections
## Container
## Container Configuration
## PHPMyAdmin
## Setting Custom Domain
## GitHub
## BitBucket
## Git from URL
## FTP
## SFTP - SSH
## Google Drive
## Dropbox
## Amazon S3
## DigitalOcean
## OneDrive

# Preferences
## Preferences Structure
## General
## Key Bindings
## FileTypes
## Linting
## Snippets

# Codeanywhere Features
## Color Picker
## Share
## Share Link
## Pair Programming
## SSH Realtime Collaboration
## Revisions
## Mini Map
## Searching and Replacing in Editor
## Find in Files
## GoTo
## Character Encoding
## Multiple Licenses
## Preview Files
## Two Factor Authentication
## Bookmarks
## Open Files
## Vim Mode
## Distraction Free Mode

# Advanced Topics
## Changing MySQL password
## Installing SASS
## Installing Laravel framework
## Installing Angular framework
## Installing Django framework
## Installing Meteor Framework
## Working with repositories
## Changing document root in container
## Subversion

# Account Management
## Purchasing a premium plan
## Addons
## Trial Plan
## Premium Plan Cancellation
## Close account

# Other
## Getting Support

