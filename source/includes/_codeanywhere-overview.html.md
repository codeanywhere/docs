# Codeanywhere Overview
## Register/Login
To get started with Codeanywhere, just Register with an account or Login if you are already registered and go to our Editor!

### Register
You can Register with Codeanywhere by selecting Sign Up on our Home page.

![](/images/signup.png)

Now you can choose between multiple registration methods:

Entering your e-mail and password which will be used upon your future sign in
* Using your Google Account
* Using your Bitbucket account
* Using your GitHub account
* Using your Facebook account

In case you choose any of the oAuth methods, you'll have to authorize Codeanywhere for it to be able to access it again.

### Login
You can log into your account if you already have an account. Simply choose between the method you used for registration and you'll be redirected to your Editor!

![](/images/signin.png)

### Forgot Password
If you forget your password, want to set an password for any of the oAuth methods, or have any problems while logging in to Codeanywhere you can use "Forgot password?" link to reset your password. It is located below login form:

![](/images/signin-forgotpassword.png)

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

![](/images/editor.png)

### The Top Menu Bar
In this section, you can find the usual menus for creating, opening and saving files, changing your view, and switching between windows.

![](/images/topmenubar.png)
Under the "Help" menu, there is a Change log button which will direct you to all the recent changes, link to our Documentation, Send Feedback button where you can send your comments and feedbacks about Codeanywhere, as well as link to our Terms of Service and Privacy Policy.

Notifications will show you all the changes made – once you create new file, share a file, or upload one, ect. On the far right you can see a Profile button.

![](/images/dashboard-access.png)

It allows you to go to your [Dashboard](#dashboard) - where you can view your subscriptions, projects and shares, change your password or delete your account - or to log off from the Editor, returning you to the Codeanywhere [homepage](https://codeanywhere.com).

### File Explorer
The File Explorer is located on the left side of the Codeanywhere Editor. Inside of the File Explorer you can find all the connections you've made with files and folders linked with them within one Project. With a right click on your Project you'll can choose if you'd like to switch an Project, share your entire Project with other users, add a new one, manage existing ones (this will redirect you to your Dashboard), add new connection within a Project, or just refresh your current Project.

![](/images/project.png)

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

![](/images/sshterminal.png)

Also, with our entirely new feature, you can collaborate directly in your terminal. Select that connection and press share in top menu bar afterwards. 

![](/images/shareicon.png)

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

```bash
sh ssh -p port cabox@hostXX.codeanyhost.com -i id_rsa.pub
```

### Status Bar
The status bar is designed to provide you with information about your code and additional functionality without getting in the way of the Editor. 
You can find the status bar in the lower part of the editor: 
 
![](/images/statusbar.png)
 
There are four pieces of information available: 
  - Position of the file which is currently opened 
  - your current row and column on the left side, which lets you know where exactly is your cursor currently placed in the code. If you click on current row, you'll be prompted to enter a line where you'd like to go.
  - Tab size let's you select your indentation - you can also change this in [General Preferences](#preferences)
  - Top right corner detects code in the file and displays it to the user. In this way user can immediately know which programming language is being used on that file for that extension - you can also change this in [FileTypes Preferences](#preferences).


## Dashboard
You can access your Dashboard from inside your Editor – just go to top menu bar and in right corner select Profile Button 

![](/images/dashboard-access.png)

Or you can go directly to [https://codeanywhere.com/dashboard](https://codeanywhere.com/dashboard).


Here, you can take care of all your Account details – manage your password, connect to various networks (GitHub, Bitbucket, Google or Facebook), and Delete your Account. 
 
![](/images/dashboard-account.png)

Under Billing, you can manage your subscriptions and purchase add-ons, check out your invoices and billing info. Also, as a security measure, here you can activate 2FA (for Freelancer Plan and higher).
 
![](/images/dashboard-billing.png)

Projects let you organize your work and using Dashboard you can access all of them, add new ones or delete old ones!
 
![](/images/dashboard-projectlist.png)

With our share feature you can work on a code with other Codeanywhere users. Now, you can access all your shares from your Dashboard – Shared with me will show you all the shares you've received!
 
![](/images/dashboard-sharedwithme.png)

In My shares, you can see all the shares you have made!

![](/images/dashboard-myshares.png)

Every Codeanywhere user has its own Public key and you can check yours by clicking in SSH keys. It can be used for secure communication with your server!


Under Custom Stacks, you can check all the Custom Stacks you've created inside your Editor!

![](/images/dashboard-customst.png)

## Projects
The Project feature allows you to organize your work into separate projects and easily switch between them without having to reload or use separate tabs. You can create as many projects as you want! 
In order to view all your projects, go to your Dashboard under section Projects. Here you can open specific project, edit them, or delete. 
When inside your Editor, just right click on your Project if you want to switch to a different one. 

![](/images/project.png)

Here, you can also create a new one, change Config of your Project, Share a Project or Manage them - this will redirect you to your [Dashboard](#dashboard). 

![](/images/dashboard-projectlist.png)
