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
The editor is the most important element of Codeanywhere and that's why we use CodeMirror. CodeMirror is a high-performance code editor for the web that supports syntax highlighting for over 100 different languages, and can still work faithfully on large documents. This is where most of the action happens. Every file you open appears as a tab on top of the Editor. You can open file easily by clicking on any file located in your File Explorer (or with a double click – depending on your preferences, you can set this up in View -> Enable Double Click).

If you want to create a new folder, right click on the connection, then choose Create folder from the expanded drop down menu. In order to create a file, also right click on a connection/folder where you'd like to create it and just enter a filename or you can double click anywhere in top editor bar. To create a specific file type, just enter the file extension (like .html, .css, .php, .js, ...) at the end of file name when creating new file (entering index.php will create an php file – it's that easy!).

Codeanywhere offers syntax highlighting for over 100 programming languages.

The code editor supports a large number of keyboard shortcuts to increase your productivity. For an up-to-date list of these within the Editor, simply go to Preferences and depending on Default, Project or User select Key bindings where you can change them.

### Terminal

With Codeanywhere you get your own Terminal/Command Prompt in the cloud. This allows you to SSH directly from your browser to a different server or compile your code all without leaving your browser. Terminal can be used to run any command on your Container or remote servers. Simply right click on your connection with SSH access and select SSH terminal. 

![](https://docs.codeanywhere.com/overview/codeanywhereui/images/sshterminal.png)

Also, with our entirely new feature, you can collaborate directly in your terminal. Select that connection and press share in top menu bar afterwards. 

![](https://docs.codeanywhere.com/overview/codeanywhereui/images/shareicon.png)

Please keep in mind that your SSH should be open. Your collaborator will receive a notification in top right corner that says: "user@mail.com has requested SSH terminal session collaboration on connection name_of_connection with you".

Use direct port access to get to Codeanywhere’s Containers via any SSH terminal or SFTP client. 

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
	3. In the Host Name field, enter the Container’s hostname (hostXX.codeanyhost.com) 
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

1. open your Terminal
2. type in ssh-keygen and you will create your public key
3. go to .ssh/id_rsa.pub and copy your entire key
4. In Codeanywhere, in Container's SSH, use command: cat .ssh/id_rsa.pub
5. use command vim authorized_keys
6. (type "A" or "I") paste your key in new line and Save (by pressing ESC, and entering :wq)
7. Check your container's /etc/ssh/sshd_config file to have 'RSAAuthentication' and 'PubkeyAuthentication' set to 'yes'
8. In case you update sshd_config file remember to restart ssh service with 'sudo service ssh restart'
9. Locate SSH port number in Container's Info

Now in order to connect to your box, you have to use the following command to create a tunnel from your local machine to your Container:

~~~~
sh ssh -p port cabox@hostXX.codeanyhost.com -i id_rsa.pub
~~~~

### Status Bar
The status bar is designed to provide you with information about your code and additional functionality without getting in the way of the Editor. 
You can find the status bar in the lower part of the editor: 
 
![](https://raw.githubusercontent.com/codeanywhere/documentation/master/overview/codeanywhereui/images/statusbar.png)
 
There are four pieces of information available: 
  - Position of the file which is currently opened 
  - your current row and column on the left side, which lets you know where exactly is your cursor currently placed in the code. If you click on current row, you'll be prompted to enter a line where you'd like to go.
  - Tab size let's you select your indentation - you can also change this in [General Preferences](#preferences)
  - Top right corner detects code in the file and displays it to the user. In this way user can immediately know which programming language is being used on that file for that extension - you can also change this in [FileTypes Preferences](#preferences).


## Dashboard
You can access your Dashboard from inside your Editor – just go to top menu bar and in right corner select Profile Button 

![](https://docs.codeanywhere.com/overview/images/dashboard-access.png)

Or you can go directly to [https://codeanywhere.com/dashboard](https://codeanywhere.com/dashboard).


Here, you can take care of all your Account details – manage your password, connect to various networks (GitHub, Bitbucket, Google or Facebook), and Delete your Account. 
 
![](https://docs.codeanywhere.com/overview/images/dashboard-account.png)

Under Billing, you can manage your subscriptions and purchase add-ons, check out your invoices and billing info. Also, as a security measure, here you can activate 2FA (for Freelancer Plan and higher).
 
![](https://docs.codeanywhere.com/overview/images/dashboard-billing.png)

Projects let you organize your work and using Dashboard you can access all of them, add new ones or delete old ones!
 
![](https://docs.codeanywhere.com/overview/images/dashboard-projectlist.png)

With our share feature you can work on a code with other Codeanywhere users. Now, you can access all your shares from your Dashboard – Shared with me will show you all the shares you've received!
 
![](https://docs.codeanywhere.com/overview/images/dashboard-sharedwithme.png)

In My shares, you can see all the shares you have made!

![](https://docs.codeanywhere.com/overview/images/dashboard-myshares.png)

Every Codeanywhere user has its own Public key and you can check yours by clicking in SSH keys. It can be used for secure communication with your server!


Under Custom Stacks, you can check all the Custom Stacks you've created inside your Editor!

![](https://docs.codeanywhere.com/overview/images/dashboard-customst.png)

## Projects
The Project feature allows you to organize your work into separate projects and easily switch between them without having to reload or use separate tabs. You can create as many projects as you want! 
In order to view all your projects, go to your Dashboard under section Projects. Here you can open specific project, edit them, or delete. 
When inside your Editor, just right click on your Project if you want to switch to a different one. 

![](https://docs.codeanywhere.com/images/project.png)

Here, you can also create a new one, change Config of your Project, Share a Project or Manage them - this will redirect you to your [Dashboard](#dashboard). 

![](https://docs.codeanywhere.com/images/dashboard-projectlist.png)

# Connections

## Container
Containers are like your own Virtual Private Servers (in essence they are OpenVZ OS containers) provisioned by Codeanywhere, each one with its own amount of RAM, Disk space and Processing power (just like any normal VPS but with some limitations such as lack of a dedicated IP address). Containers give you the ability to provision any Development Environment you like. You can choose between one of the predefined stacks:

* Default – Blank Development Container
* PHP – LAMP Development Stack with phpMyAdmin and Composer preinstalled
* NodeJS – NodeJS Development Stack with npm and yarn preinstalled
* Ruby – Ruby Development Stack with RVM and Ruby on Rails preinstalled
* Python – Python Development Stack with pyenv, pip and virtualenv preinstalled
* C/C++ – C/C++ Development Stack with gcc and g++ compiler and gdb preinstalled
* HTML – HTML5 Development Stack with Apache, Node.js and npm preinstalled
* Wordpress – LAMP Development Stack with Wordpress, phpMyAdmin and Composer preinstalled
* Java – Java Development Stack with OpenJDK7, OpenJDE7 and Tomcat7 preinstalled
* .NET Core – .NET Core Development Stack

You won't even be aware of it being created or started. You can choose between two operating systems: Ubuntu 16.04 and CentOS 7.2.

![](https://docs.codeanywhere.com/connections/images/container-create.png)

Also, if you require any development environment you can't find in our list, you can create a container from a Blank stack and install anything you want and you can find some popular stacks installation steps in our Advanced Topics section. Afterwards, just save it as a Custom Stack and you can use it again and again! The best part of Containers is that not only does it remove issue of having your development environment wherever you are; it also enables you to connect to any GIT repository in the world, be it a corporate server or popular services like GitHub or Bitbucket. With Containers you can now finally connect to your repositories and use its full capabilities, so now you can use commit to repositories from Codeanywhere!

Create a new Container by going to File -> New Connection -> Container

![](https://docs.codeanywhere.com/connections/images/container-open.png)

Choose your environment, name it and click Create!

![](https://docs.codeanywhere.com/connections/images/container-php.png)

### Manage Container

![](https://docs.codeanywhere.com/connections/images/container-manage.png)

With Container get SSH access to your Container and you can use all the necessary actions such as git commands, installation of new depencencies ect! You can Turn Off or Turn On your Box, restart it or set it to be Always On so you can access your Box at anytime, without the need of logging into your account and starting it. With containers, you can view your code with your preview link. You can check your preview link inside Info.

![](https://docs.codeanywhere.com/connections/images/container-info.png)

Be sure to replace the XX with the port you have specified in your app.

In Config, you can set up commands necessary for your Stack to Run. Custom Stack can be created out of any Container! If you installed anything using your terminal, just save it as a Custom Stack and use it again and again. This way, you don't have to lose anytime for creating your development environment all over again!

By selecting Run, your preview link will be opened and any command neccessary to run your app, opened in SSH terminal.

Create any file, by entering filename.extension, or folder inside your container, Upload files directly from your local storage or Share your entire Container!

In case you want to delete your entire Container, just click Destroy. However, keep in mind that your work will be removed and you wont be able to retrieve it afterwards!

### Creating a Custom Stack

In order to create a Custom Stack of one of your Stacks, first, you'll have to right click on your Container and select Create Custom Stacks

![](https://docs.codeanywhere.com/connections/images/ccs1.png)

Enter your File name and Description so you could find it easier later on!

![](https://docs.codeanywhere.com/connections/images/ccs2.png)

You can access all your Custom Stacks in your [Dashboard](#dashboard).

### Deploy to Heroku

Deploying with Heroku requires you to install Heroku toolbelt. You can install it using SSH command:

~~~~
wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh
~~~~

Now you can use Heroku CLI. More detailed instruction can be found on official Heroku toolbelt website [https://toolbelt.heroku.com/](https://toolbelt.heroku.com/)

### Locate Private and Public

You can view Keys of your container by going to cd /home/cabox/.ssh/ using your SSH terminal. There you will find:

* id_rsa - private key container of your container,
* id_rsa.pub - public key of your container.

### Connect your Container via SSH

![](https://docs.codeanywhere.com/connections/images/container-hostname.png)

These are the credentials you'll need:

* Hostname and port: check it in Container's Info with a right click on your Container, select Info, locate SSH access, and that's the hostname and port you have to use.
* User name: cabox
* As for the password, you can't connect this way. You'll need private key of your Container and you can get it by going to /home/cabox/.ssh/id_rsa and that's your private key which you can use for connecting to your Container.

Containers are available to all users, just login and try it out!

## Container Configuration

Right click on your Container and you will see your dropdown menu:

![](https://docs.codeanywhere.com/connections/images/container-manage.png)

With Container get SSH access to your Container and you can use all the necessary actions such as git commands, installation of new depencencies ect! You can Turn Off or Turn On your Box, restart it or set it to be Always On so you can access your Box at anytime, without the need of logging into your account and starting it.

With containers, you can view your code with your preview link. You can check your preview link inside Info.

![](https://docs.codeanywhere.com/connections/images/container-info.png)

You can use your preview link or, if you want to used the one with specified port, be sure to replace the XX with the port you have specified in your app. Also, you can add ":port_number" at the end of your preview link.

In Config, you can set up commands necessary for your Stack to Run.

Let's say, you have an app inside your workspace folder /path/to/folder/. By default current working dir is set to be /workspace/. By changing "cwd": "~/workspace" to "cwd": "~/workspace/path/to/folder", you can set the file path which will be used upon running your app.

cwd (curent working directory) is the location in which your run commands should be located. The default location is ~/workspace, if your commands are located in a subdirectory named "test” then cwd should be ~/workspace/test.

![](https://docs.codeanywhere.com/connections/images/container-config-cwd.png)

NOTE: containers hosting content via Apache (example: html, php) expect that content to be located at ~/workspace, if you keep your content in another directory you should edit or create the ~/workspace/.htaccess file to point at that directory.

Inside "commands" you can set any commands necesary for running your container.

In "commands": [], set command neccessary for running your app, such as: "grunt", "ember server", "rails server" ect, depending on your app.

![](https://docs.codeanywhere.com/connections/images/container-config-commands.png)

If you changed port in your app, to listen to the port defined in your Config file, under "environment", feel free to set new port number which will use your app.

By selecting Run, your preview link will be opened and any command neccessary to run your app, opened in SSH terminal.

### Running on Localhost

Some of our stacks will default the IP to the localhost: 127.0.0.1. You have to change the default IP so your Container could run externally. Please change IP address on your container from 127.0.0.1 to 0.0.0.0 so that you could be able to preview your Ruby box. You can do that inside Config - under commands - of your container (right click on your container and select Config).

For example, on Ruby stack, you just have to use the following command in order to run your Rails container: "rails s --binding=0.0.0.0" This will override localhost (127.0.0.1) where your app can't work. And now, you'll be able to view your Ruby app on: preview.xxxxxx.box.codeanywhere.com:3000.

### Locate Private and Public

You can view Keys of your container by going to cd /home/cabox/.ssh/ using your SSH terminal. There you will find:

* id_rsa - private key container of your container,
* id_rsa.pub - public key of your container.

## PHPMyAdmin

PhpMyAdmin comes preinstalled with our Containers (both CentOS and Ubuntu). To access it first open the info by right-clicking the Container in File Explorer:

![](https://docs.codeanywhere.com/connections/images/container-info.png)

At the top of your Info page, you can see your Username and Password. Copy the link into the new tab of your browser and add „/phpmyadmin“ at the end of the link to access phpMyAdmin – it will look something like: [http://preview.xxxxxx.box.codeanywhere.com/phpmyadmin](http://preview.xxxxxx.box.codeanywhere.com/phpmyadmin) or, in this example, [http://port-80.xxxxxx.box.codeanywhere.com/phpmyadmin](http://port-80.xxxxxx.box.codeanywhere.com/phpmyadmin). For login use the "root" as Username, and leave the Password field empty:

![](https://docs.codeanywhere.com/connections/images/phpmyadmin.png)

Username and password will vary depending on the Stack you choose! You can check it in your Info file in first line.

If you want to be able to access your Container at all times, you can activate our feature Always-on, which will keep your Container running even when you're not using Codeanywhere!

## Setting Custom Domain

Once you've created a container, you will probably want to preview it in your own link! Now, you can set your custom domain using our [Dashboard](#dashboard)!

![](https://docs.codeanywhere.com/connections/images/customdomain1.png)

### CNAME Records

Before you start configuring your domain in Codeanywhere, there is one step you should do first and that is to go to your domain register (GoDaddy and similar) and create a CNAME record.

The CNAME record you create must point to our proxy server: sfo.codeanyproxy.com

For more information on CNAMEs and how they work, please visit the Google Support Guide for CNAME records.

In your dashboard, select "Add New Domain Name".

### Add your Custom Domain

Add External Port to 80, 443 or port in range of 1024 and 9999. Set the Internal Port to the port your application server is listening to. For example, if you set your Internal Port to 8000 and External Port to 80, you can access your custom domain without appending :8000 at the URL.

![](https://docs.codeanywhere.com/connections/images/customdomain1-1.png)

If you set the External port to 443, Codeanywhere will automatically set up a free SSL certificate provided by Let's Encrypt! It is important that you have already configured your CNAME record to point to Codeanywhere proxy server so the certificate can be issued.

![](https://docs.codeanywhere.com/connections/images/customdomain2.png)

Click on Create and that's it! Now you can access your Container from your domain! Custom domains do not prevent container to be turned off in case it does not have AlwaysOn feature enabled.

## GitHub

With Codeanywhere, you’ll be able to work directly with your GitHub repositories. Codeanywhere will create a [Container](#container) for each repository and you will be able to edit your code directly from there. Containers are in essence your own Virtual Private Servers run invisibly in the background of Codeanywhere, each one with its own amount of RAM, Disk space and Processing power. DevBoxes give you the ability to provision any Development Environment you like or you can select between the number of our predefined stacks! You won't even be aware of it being created or started. After your repositroy is imported, you can edit and preview your code. Then, you can push changes back to your repo using your SSH Terminal! Just check our [Working with Repositories](#working-with-repositories) section for further instructions.

### Creating an GitHub Container
Go to File -> New Connection -> GitHub.

![](https://docs.codeanywhere.com/connections/images/github-open.png)

After selecting it, Add GitHub Access window appears. Click on "Connect your GitHub Account" in order to proceed.

![](https://docs.codeanywhere.com/connections/images/github-connect.png)

Enter your GitHub account details to connect to your GitHub account and authorize Codeanywhere for quick and easy access.

![](https://docs.codeanywhere.com/connections/images/githubauth.png)

You’ll be prompted which repository you want to connect to.

![](https://docs.codeanywhere.com/connections/images/github-repo.png)

Just select repository you want to access, setup your development environment, or let our system decide for you!

![](https://docs.codeanywhere.com/connections/images/github-repo2.png)

Now you’ve created a new [Container](#container) with your repository!

Once you have got the repo in Codeanywhere, you can work on it from anywhere. You'll be able to edit your files, or run projects within Codeanywhere!

### Accessing GitHub Organizations
You have to explicitly allow Codeanywhere to access your organizations. You can do it in two ways:

1. During authorization process Click Grant / Request Access on organization which repositories you want to access through Codeanywhere
	![](https://docs.codeanywhere.com/connections/images/pic1.png)
2. While logged in your GitHub account, click Account -> Settings -> Applications -> Codeanywhere Click Grant / Request Access on organization which repositories you want to access through Codeanywhere
	![](https://docs.codeanywhere.com/connections/images/pic2.png)

After allowing organization access, you can list your repositories through Codeanywhere.

### Working with repositories

You can push changes to Github using standard git commands inside your SSH terminal:

~~~~
git add -A // To track all files
~~~~

~~~~
git commit -am "message" // To commit changes
~~~~

~~~~
git push origin master // Push your local changes to github
~~~~

## BitBucket

With Codeanywhere, you’ll be able to work directly with your Bitbucket repositories. Codeanywhere will create a [Container](#container) for each repository and you will be able to edit your code directly from there. Containers are in essence your own Virtual Private Servers run invisibly in the background of Codeanywhere, each one with its own amount of RAM, Disk space and Processing power. DevBoxes give you the ability to provision any Development Environment you like or you can select between the number of our predefined stacks! You won't even be aware of it being created or started. 
After your repositroy is imported, you can edit and preview your code. Then, you can push changes back to your repo using your SSH Terminal! Just check our [Working with Repositories section](#working-with-repositories) for further instructions.


### Creating an Bitbucket Container

Go to File -> New Connection -> Bitbucket:

![bitbucket-open](https://docs.codeanywhere.com/connections/images/bitbucket-open.png)

After selecting it, Add Bitbucket Access window appears. Click on "Connect your Bitbucket Account" in order to proceed.

![bitbucket-connect](https://docs.codeanywhere.com/connections/images/bitbucket-connect.png)

Enter Bitbucket details to connect to your Bitbucket account and authorize Codeanywhere for quick and easy access.

![bitbucket-authorize](https://docs.codeanywhere.com/connections/images/bitbucket-authorize.png)

You’ll be prompted which repository you want to connect to.

![bitbucket-repo](https://docs.codeanywhere.com/connections/images/bitbucket-repo.png)

Now just select repository you want to access, setup your development environment, or let our system decide for you!

![bitbucket-repo2](https://docs.codeanywhere.com/connections/images/bitbucket-repo2.png)

Now you’ve created a new [Container](http://docs.codeanywhere.com/connections/container.html) with your repository!

Once you have got the repo in Codeanywhere, you can work on it from anywhere. You'll be able to edit your files, or run projects within Codeanywhere!


### Bitbucket SSH key

You can link your Codeanywhere SSH key to your Bitbucket account. That way, you can push commits to your private repo without password prompt. To do so, copy your [Codeanywhere public key](#ssh-keys) and paste it to your Bitbucket account (Account -> manage account -> SSH keys -> add Key)

Now your Codeanywhere account is authorized to make changes to your repo.

If you already have repository in Bitbucket, just by cloning your repository, your git will be setup. If you have existing project with empty Bitbucket git repository, you can add your repo with "git remote add origin {GIT_SSH_URL}". You can find your {GIT_SSH_URL} by clicking clone in bitbucket repo, then copying url next to 'git clone', its format is git@bitbucket.org:/username/repository.git

### Working with repositories

You can push changes to Bitbucket using standard git commands inside your SSH terminal:

~~~~
git add -A // To track all files
~~~~

~~~~
git commit -am "message" // To commit changes
~~~~

~~~~
git push origin master // Push your local changes to bitbucket
~~~~

For more information see [working with repositories](#working-with-repositories)

## Git from URL

Codeanywhere will create a [Container](#container) for each repository and you will be able to edit your code directly from there. Then, you can push changes back to your repo using your SSH Terminal! Just check our [Working with Repositories](#working-with-repositories) section for further instructions.

### Creating an Git Container from URL
Go to File -> New Connection -> GitFromURL

![](https://docs.codeanywhere.com/connections/images/gitfromurl-open.png)

You can connect to your repository by entering your repository url in Git from URL form!

![](https://docs.codeanywhere.com/connections/images/gitfromurl-connect.png)

Select a Stack and a name and you’ve created a new [Container](#container) with your repository!

### Working with repositories

~~~~
git add -A // To track all files
~~~~

~~~~
git commit -am "message" // To commit changes
~~~~

~~~~
git push origin master // Push your local changes
~~~~

## FTP
With Codeanywhere, you can connect your existing FTP/FTPs server!

### Adding an existing FTP/FTPs
Go to File -> New Connection -> FTP.

![](https://docs.codeanywhere.com/connections/images/ftpserver-open.png)

After selecting it, Add FTP window appears where you enter server information and add that server to your Project for quick and easy access.

![](https://docs.codeanywhere.com/connections/images/ftpserver-connect.png)

* Server name - the name which will be shown in File Explorer, it is user definable, meaning you can name your server however you want
* Hostname - the hostname or IP address of your server (example: ftp.mywebsite.com)
* Username - username of your FTP/FTPS server
* Password - password of your FTP/FTPS server
* Type - choose between FTP or FTPs -- if FTPs is selected, choose Authentication Type: Explicit FTP over TLS or Implicit FTP over TLS
* Initial dir - set path
* Timeout - default: 20
* Port - default: 21

Your FTP/FTPs server will be automatically added to the File Explorer with an FTP icon.

### Managing FTP/FTPs
If you right-click on any FTP server listed, it will expand a menu offering more options: Rename, Permissions, Refresh, Create File, Create Folder, Upload, Share, Remove and Settings – where you can change your FTP/FTPs credentials.

![](https://docs.codeanywhere.com/connections/images/ftpserver-manage.png)

To access SSH terminal, simply add an SSH connection instead and you'll have all the features of your FTP with SSH terminal! Right-clicking folders and files gives you some additional options such as Copy and Cut, to simplify managing of files and folders – still you can simply Drag and Drop your files in order to move them between folders and even Connections!

### Local FTP or FTPS
Codeanywhere uses its file services in the cloud that are used for making connections. Behind the scenes it looks something like this:

Codeanywhere Web or mobile app ----> Codeanywhere API ----> Codeanywhere File Service ----> Your FTP/FTPS Server

If your FTP/FTPS server is in your local network, the only way you could connect to your server from Codeanywhere is that you use port forwarding on your router to your local FTP/FTPS server. The other problem that could come in your case is your router's public IP. If your internet provider does not provide you a static IP, then you would also need to use some of DDNS services.

### Server response
Codeanywhere is acting as a "middle man" between user and your server - any action done by user is firstly processed at our server and then sent to your server. Same thing works in opposite direction, your server sends response to Codeanywhere and then Codeanywhere forwards the response back to user. Also, the speed of the server response depends on the server location. If your server is located it America, the response will be faster, but if it's located in China it will be slower. We do plan to expand our server coverage around the world for faster connections!

### IP Whitelist

While performing actions using Codeanywhere, the requests are sent from our app to your server. You must make sure that your server is reachable from the following IP addresses:

* 65.52.184.164
* 51.141.5.180
* 52.161.27.120
* 54.187.136.143
* 54.187.142.118
* 54.187.182.165
* 54.187.44.75

If you have no administration rights on the server, please ask your administrator whitelist these IP’s.

## SFTP - SSH
With Codeanywhere, you can connect your existing SFTP/SSH server!

### Adding an existing SSH
Go to File -> New Connection -> SFTP-SSH.

![](https://docs.codeanywhere.com/connections/images/sshserver-open.png)

After selecting it, Add SSH window appears where you enter server information and add that server to your Project for quick and easy access.

* Server name - the name which will be shown in File Explorer, it is user definable, meaning you can name your server however you want
* Hostname - the hostname or IP address of your server (example: ssh.mywebsite.com)
* Username - username of your SSH/SFTP server
* Password - password of your SSH/SFTP server
* Authentication - use different type of authentication: Password, Public Key, Private Key
* Initial dir - set path
* Timeout - default: 20
* Port - default: 22

![](https://docs.codeanywhere.com/connections/images/sshserver-connect1.png)

Your SFTP-SSH server will be automatically added to the File Explorer with an SSH icon. If you right-click on any server listed, it will expand a menu offering more options: Rename, Permissions, Refresh, Create File, Create Folder, Upload, Share, Remove and Settings – where you can change your credentials.

### Local SSH or SFTP
Codeanywhere uses its file services in the cloud that are used for making connections. Behind the scenes it looks something like this:

Codeanywhere Web or mobile app ----> Codeanywhere API ----> Codeanywhere File Service ----> Your SFTP-SSH Server

If your server is in your local network, the only way you could connect to your server from Codeanywhere is that you use port forwarding on your router to your local SSH server. The other problem that could come in your case is your router's public IP. If your internet provider does not provide you a static IP, then you would also need to use some of DDNS services.

### Server response
While working with FileZilla you are directly connected from local computer to your server, on the other hand the Codeanywhere is acting as a "middle man" between user and SFTP-SSH - any action done by user is firstly processed at our server and then sent to the your server. Same thing works in opposite direction, server sends response to Codeanywhere and then Codeanywhere forwards the response back to user. Also, the speed of the server response depends on the server location. If your server is located it America, the response will be faster, but if it's located in China it will be slower. We do plan to expand our server coverage around the world for faster connections!

### IP whitelist
While performing actions using Codeanywhere, the requests are sent from our app to your server. You must make sure that your server is reachable from the following IP addresses:

* 65.52.184.164
* 51.141.5.180
* 52.161.27.120
* 54.187.136.143
* 54.187.142.118
* 54.187.182.165
* 54.187.44.75

If you have no administration rights on the server, please ask your administrator to whitelist these IP’s.

## Google Drive
With Codeanywhere, you can connect your Google Drive account!

### Adding a New Connection to Google Drive
Go to File -> New Connections -> Google Drive.

![](https://docs.codeanywhere.com/connections/images/googledrive-open.png)

After selecting it, Add Google Drive Access window appears. Click on "Add your Google Drive Account" in order to proceed.

![](https://docs.codeanywhere.com/connections/images/googledrive-connect.png)

Enter your Google Drive account details to add that Google Drive account to your server list for quick and easy access.

![](https://docs.codeanywhere.com/connections/images/googlelogin.png)

If the Google Drive account is added successfully it will appear in your File Explorer with the Google Drive icon. Now you can easily edit files from your Google Drive account!

### Invalid Token issue
If you receive an Invalid Token error, it means there is something wrong with your long-term access token, so please try removing and adding your Drive account. If that does not work please try revoking access to Codeanywhere from your Google security page located at: [https://www.google.com/settings/security](https://www.google.com/settings/security) - under Connected apps and sites, Remove Codeanywhere, and afterwards add it again.

![](https://docs.codeanywhere.com/connections/images/google-invalidtoken.png)

## Dropbox

With Codeanywhere, you can connect your Dropbox account!

### Adding a New Connection to Dropbox
Go to File -> New Connections -> Dropbox.

![](https://docs.codeanywhere.com/connections/images/dropbox-open.png)

After selecting it, Add Dropbox Access window appears. Click on "Add your Dropbox Account" in order to proceed.

![](https://docs.codeanywhere.com/connections/images/dropbox-connect.png)

Enter your Dropbox account details to add that Dropbox account to your server list for quick and easy access.

![](https://docs.codeanywhere.com/connections/images/dropbox-authorize.png)

If the Dropbox account is added successfully it will appear in your File Explorer with the Dropbox icon!

## Amazon S3
Amazon's S3 is integrated into Codeanywhere just as FTP, Dropbox, and Google Drive.

### Creating Amazon S3 connection
Go to File -> New Connections -> Amazon S3.

![](https://docs.codeanywhere.com/connections/images/amazons3-open.png)

After selecting it, enter credentials of your S3 Bucket:

![](https://docs.codeanywhere.com/connections/images/amazons3-connect.png)

* Server - name of your AmazonS3 Server
* Bucket - name of your AmazonS3 Bucket
* Access Key ID - a alphanumeric text string that uniquely identifies the user who owns the account
* Secret Access Key - password of an AmazonS3 account

If the S3 account is added successfully it will appear in your File Explorer with the S3 icon.

## DigitalOcean

With Codeanywhere, you can work directly with your DigitalOcean Droplets!

### Adding a New Connection to DigitalOcean
In order to create a new Droplet using Codeanywhere, simply go to File -> New Connection -> DigitalOcean.

![](https://docs.codeanywhere.com/connections/images/digitalocean-open.png)

After selecting DigitalOcean, Add DigitalOcean Access window appears. Click on "Connect your DigitalOcean Account" in order to proceed.

![](https://docs.codeanywhere.com/connections/images/digitalocean-connect.png)

Enter your Digital Ocean account details to log in and connect to your Digital Ocean account and authorize Codeanywhere for quick and easy access!

![](https://docs.codeanywhere.com/connections/images/digitalocean-authorize.png)

Now, in your Editor, you’ll be able to create a new Droplet which will be added to your Digital Ocean account.

### Creating a new Droplet
First of all, you can select your new Droplet image from 4 categories: Distributions, One-click Apps, Snapshots and Backups. Also, here, you can select Droplet’s Size, as well as Region of your Droplet - the same way you do that with Digital Ocean!

![](https://docs.codeanywhere.com/connections/images/do-droplet-create1.png)

After selecting Next, you can enter Host name of your Droplet which will also be shown in your Codeanywhere file tree, as well as in your Digital Ocean account, SSH Keys you’d like to import and any Additional Add-on you’d like to select.

![](https://docs.codeanywhere.com/connections/images/do-droplet-create2.png)

Click Create and your Droplet will be added into your Codeanywhere account and to your Digital Ocean account!

### Managing a Droplet

![](https://docs.codeanywhere.com/connections/images/do-droplet-manage.png)

With Codeanywhere, you get SSH access to your Droplet and you can use all the necessary actions! Also, you can use other actions:

* Turn Off / Start - power off your Droplet at any time and turn it on again,
* Restart - reboot your Droplet,
* Settings - change settings of your Droplet,
* Rename - change Host name,
* Refresh - refresh Droplet,
* Create File - create file directly in a Droplet, just enter name and extension of your file,
* Create Folder - create folder directly in a Droplet,
* Upload - simply upload from your local machine into your Droplet,
* Share - share your Droplet with other users for collaboration, or if you just want them to view your Droplet
* Remove - remove your Droplet from Codeanyhwere. It will still remain active in your Digital Ocean account.

You can check these options by right clicking on your new Droplet in Codeanywhere.

### What happens when you delete a Droplet outside of Codeanywhere’s UI?
When you delete a Droplet outside of Codeanywhere’s UI, you’ll receive the following message next to your Droplet in your File Tree: “Error:Droplet Not Found”, and you won’t be able to access it anymore since it is destroyed.

![](https://docs.codeanywhere.com/connections/images/do-droplet-deleted.png)

Keep in mind, that if you use Codeanywhere to Remove your Droplet, it will disappear from your Codeanywhere account, but you’ll still be able to access it using Digital Ocean.

### Adding authorization to a different account
If you want to remove authorization for your Digital Ocean account, go to your Dashboard and under Account, select Disconnect from your current Digital Ocean account.

![](https://docs.codeanywhere.com/connections/images/do-droplet-dashboard.png)

Now, you can authorize different Digital Ocean account by simply Connecting to a different one - the same way as described before, or if you’re already logged in Digital Ocean account, directly from your Dashboard.

### Adding existing Droplet
While creating a Droplet via Codeanywhere, we have a full integration, and connection of an existing Droplet is possible by using SSH connection. While connecting via [SSH server](#sftp-ssh), you have to take your CA public key and implement it inside authenticated_keys.

## OneDrive

With Codeanywhere, you can connect your OneDrive account!

### Adding a New Connection to OneDrive
Go to File -> New Connections -> OneDrive.

![](https://docs.codeanywhere.com/connections/images/onedrive-open.png)

After selecting it, Add OneDrive Access window appears. Click on "Add your OneDrive Account" in order to proceed.

![](https://docs.codeanywhere.com/connections/images/onedrive-connect.png)

Enter your OneDrive account details to add that OneDrive account to your server list for quick and easy access.

![](https://docs.codeanywhere.com/connections/images/onedrive-login.png)

If the OneDrive account is added successfully it will appear in your File Explorer with the OneDrive icon. Now you can easily edit files from your OneDrive account!

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

