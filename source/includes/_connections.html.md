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

![](/images/container-create.png)

Also, if you require any development environment you can't find in our list, you can create a container from a Blank stack and install anything you want and you can find some popular stacks installation steps in our Advanced Topics section. Afterwards, just save it as a Custom Stack and you can use it again and again! The best part of Containers is that not only does it remove issue of having your development environment wherever you are; it also enables you to connect to any GIT repository in the world, be it a corporate server or popular services like GitHub or Bitbucket. With Containers you can now finally connect to your repositories and use its full capabilities, so now you can use commit to repositories from Codeanywhere!

Create a new Container by going to File -> New Connection -> Container

![](/images/container-open.png)

Choose your environment, name it and click Create!

![](/images/container-php.png)

### Manage Container

![](/images/container-manage.png)

With Container get SSH access to your Container and you can use all the necessary actions such as git commands, installation of new depencencies ect! You can Turn Off or Turn On your Box, restart it or set it to be Always On so you can access your Box at anytime, without the need of logging into your account and starting it. With containers, you can view your code with your preview link. You can check your preview link inside Info.

![](/images/container-info.png)

Be sure to replace the XX with the port you have specified in your app.

In Config, you can set up commands necessary for your Stack to Run. Custom Stack can be created out of any Container! If you installed anything using your terminal, just save it as a Custom Stack and use it again and again. This way, you don't have to lose anytime for creating your development environment all over again!

By selecting Run, your preview link will be opened and any command neccessary to run your app, opened in SSH terminal.

Create any file, by entering filename.extension, or folder inside your container, Upload files directly from your local storage or Share your entire Container!

In case you want to delete your entire Container, just click Destroy. However, keep in mind that your work will be removed and you wont be able to retrieve it afterwards!

### Creating a Custom Stack

In order to create a Custom Stack of one of your Stacks, first, you'll have to right click on your Container and select Create Custom Stacks

![](/images/ccs1.png)

Enter your File name and Description so you could find it easier later on!

![](/images/ccs2.png)

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

![](/images/container-hostname.png)

These are the credentials you'll need:

* Hostname and port: check it in Container's Info with a right click on your Container, select Info, locate SSH access, and that's the hostname and port you have to use.
* User name: cabox
* As for the password, you can't connect this way. You'll need private key of your Container and you can get it by going to /home/cabox/.ssh/id_rsa and that's your private key which you can use for connecting to your Container.

Containers are available to all users, just login and try it out!

## Container Configuration

Right click on your Container and you will see your dropdown menu:

![](/images/container-manage.png)

With Container get SSH access to your Container and you can use all the necessary actions such as git commands, installation of new depencencies ect! You can Turn Off or Turn On your Box, restart it or set it to be Always On so you can access your Box at anytime, without the need of logging into your account and starting it.

With containers, you can view your code with your preview link. You can check your preview link inside Info.

![](/images/container-info.png)

You can use your preview link or, if you want to used the one with specified port, be sure to replace the XX with the port you have specified in your app. Also, you can add ":port_number" at the end of your preview link.

In Config, you can set up commands necessary for your Stack to Run.

Let's say, you have an app inside your workspace folder /path/to/folder/. By default current working dir is set to be /workspace/. By changing "cwd": "~/workspace" to "cwd": "~/workspace/path/to/folder", you can set the file path which will be used upon running your app.

cwd (curent working directory) is the location in which your run commands should be located. The default location is ~/workspace, if your commands are located in a subdirectory named "test” then cwd should be ~/workspace/test.

![](/images/container-config-cwd.png)

NOTE: containers hosting content via Apache (example: html, php) expect that content to be located at ~/workspace, if you keep your content in another directory you should edit or create the ~/workspace/.htaccess file to point at that directory.

Inside "commands" you can set any commands necesary for running your container.

In "commands": [], set command neccessary for running your app, such as: "grunt", "ember server", "rails server" ect, depending on your app.

![](/images/container-config-commands.png)

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

![](/images/container-info.png)

At the top of your Info page, you can see your Username and Password. Copy the link into the new tab of your browser and add „/phpmyadmin“ at the end of the link to access phpMyAdmin – it will look something like: [http://preview.xxxxxx.box.codeanywhere.com/phpmyadmin](http://preview.xxxxxx.box.codeanywhere.com/phpmyadmin) or, in this example, [http://port-80.xxxxxx.box.codeanywhere.com/phpmyadmin](http://port-80.xxxxxx.box.codeanywhere.com/phpmyadmin). For login use the "root" as Username, and leave the Password field empty:

![](/images/phpmyadmin.png)

Username and password will vary depending on the Stack you choose! You can check it in your Info file in first line.

If you want to be able to access your Container at all times, you can activate our feature Always-on, which will keep your Container running even when you're not using Codeanywhere!

## Setting Custom Domain

Once you've created a container, you will probably want to preview it in your own link! Now, you can set your custom domain using our [Dashboard](#dashboard)!

![](/images/customdomain1.png)

### CNAME Records

Before you start configuring your domain in Codeanywhere, there is one step you should do first and that is to go to your domain register (GoDaddy and similar) and create a CNAME record.

The CNAME record you create must point to our proxy server: sfo.codeanyproxy.com

For more information on CNAMEs and how they work, please visit the Google Support Guide for CNAME records.

In your dashboard, select "Add New Domain Name".

### Add your Custom Domain

Add External Port to 80, 443 or port in range of 1024 and 9999. Set the Internal Port to the port your application server is listening to. For example, if you set your Internal Port to 8000 and External Port to 80, you can access your custom domain without appending :8000 at the URL.

![](/images/customdomain1-1.png)

If you set the External port to 443, Codeanywhere will automatically set up a free SSL certificate provided by Let's Encrypt! It is important that you have already configured your CNAME record to point to Codeanywhere proxy server so the certificate can be issued.

![](/images/customdomain2.png)

Click on Create and that's it! Now you can access your Container from your domain! Custom domains do not prevent container to be turned off in case it does not have AlwaysOn feature enabled.

## GitHub

With Codeanywhere, you’ll be able to work directly with your GitHub repositories. Codeanywhere will create a [Container](#container) for each repository and you will be able to edit your code directly from there. Containers are in essence your own Virtual Private Servers run invisibly in the background of Codeanywhere, each one with its own amount of RAM, Disk space and Processing power. DevBoxes give you the ability to provision any Development Environment you like or you can select between the number of our predefined stacks! You won't even be aware of it being created or started. After your repositroy is imported, you can edit and preview your code. Then, you can push changes back to your repo using your SSH Terminal! Just check our [Working with Repositories](#working-with-repositories) section for further instructions.

### Creating an GitHub Container
Go to File -> New Connection -> GitHub.

![](/images/github-open.png)

After selecting it, Add GitHub Access window appears. Click on "Connect your GitHub Account" in order to proceed.

![](/images/github-connect.png)

Enter your GitHub account details to connect to your GitHub account and authorize Codeanywhere for quick and easy access.

![](/images/githubauth.png)

You’ll be prompted which repository you want to connect to.

![](/images/github-repo.png)

Just select repository you want to access, setup your development environment, or let our system decide for you!

![](/images/github-repo2.png)

Now you’ve created a new [Container](#container) with your repository!

Once you have got the repo in Codeanywhere, you can work on it from anywhere. You'll be able to edit your files, or run projects within Codeanywhere!

### Accessing GitHub Organizations
You have to explicitly allow Codeanywhere to access your organizations. You can do it in two ways:

1. During authorization process Click Grant / Request Access on organization which repositories you want to access through Codeanywhere
	![](/images/pic1.png)
2. While logged in your GitHub account, click Account -> Settings -> Applications -> Codeanywhere Click Grant / Request Access on organization which repositories you want to access through Codeanywhere
	![](/images/pic2.png)

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

![bitbucket-open](/images/bitbucket-open.png)

After selecting it, Add Bitbucket Access window appears. Click on "Connect your Bitbucket Account" in order to proceed.

![bitbucket-connect](/images/bitbucket-connect.png)

Enter Bitbucket details to connect to your Bitbucket account and authorize Codeanywhere for quick and easy access.

![bitbucket-authorize](/images/bitbucket-authorize.png)

You’ll be prompted which repository you want to connect to.

![bitbucket-repo](/images/bitbucket-repo.png)

Now just select repository you want to access, setup your development environment, or let our system decide for you!

![bitbucket-repo2](/images/bitbucket-repo2.png)

Now you’ve created a new [Container](/container.html) with your repository!

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

![](/images/gitfromurl-open.png)

You can connect to your repository by entering your repository url in Git from URL form!

![](/images/gitfromurl-connect.png)

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

![](/images/ftpserver-open.png)

After selecting it, Add FTP window appears where you enter server information and add that server to your Project for quick and easy access.

![](/images/ftpserver-connect.png)

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

![](/images/ftpserver-manage.png)

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

![](/images/sshserver-open.png)

After selecting it, Add SSH window appears where you enter server information and add that server to your Project for quick and easy access.

* Server name - the name which will be shown in File Explorer, it is user definable, meaning you can name your server however you want
* Hostname - the hostname or IP address of your server (example: ssh.mywebsite.com)
* Username - username of your SSH/SFTP server
* Password - password of your SSH/SFTP server
* Authentication - use different type of authentication: Password, Public Key, Private Key
* Initial dir - set path
* Timeout - default: 20
* Port - default: 22

![](/images/sshserver-connect1.png)

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

![](/images/googledrive-open.png)

After selecting it, Add Google Drive Access window appears. Click on "Add your Google Drive Account" in order to proceed.

![](/images/googledrive-connect.png)

Enter your Google Drive account details to add that Google Drive account to your server list for quick and easy access.

![](/images/googlelogin.png)

If the Google Drive account is added successfully it will appear in your File Explorer with the Google Drive icon. Now you can easily edit files from your Google Drive account!

### Invalid Token issue
If you receive an Invalid Token error, it means there is something wrong with your long-term access token, so please try removing and adding your Drive account. If that does not work please try revoking access to Codeanywhere from your Google security page located at: [https://www.google.com/settings/security](https://www.google.com/settings/security) - under Connected apps and sites, Remove Codeanywhere, and afterwards add it again.

![](/images/google-invalidtoken.png)

## Dropbox

With Codeanywhere, you can connect your Dropbox account!

### Adding a New Connection to Dropbox
Go to File -> New Connections -> Dropbox.

![](/images/dropbox-open.png)

After selecting it, Add Dropbox Access window appears. Click on "Add your Dropbox Account" in order to proceed.

![](/images/dropbox-connect.png)

Enter your Dropbox account details to add that Dropbox account to your server list for quick and easy access.

![](/images/dropbox-authorize.png)

If the Dropbox account is added successfully it will appear in your File Explorer with the Dropbox icon!

## Amazon S3
Amazon's S3 is integrated into Codeanywhere just as FTP, Dropbox, and Google Drive.

### Creating Amazon S3 connection
Go to File -> New Connections -> Amazon S3.

![](/images/amazons3-open.png)

After selecting it, enter credentials of your S3 Bucket:

![](/images/amazons3-connect.png)

* Server - name of your AmazonS3 Server
* Bucket - name of your AmazonS3 Bucket
* Access Key ID - a alphanumeric text string that uniquely identifies the user who owns the account
* Secret Access Key - password of an AmazonS3 account

If the S3 account is added successfully it will appear in your File Explorer with the S3 icon.

## DigitalOcean

With Codeanywhere, you can work directly with your DigitalOcean Droplets!

### Adding a New Connection to DigitalOcean
In order to create a new Droplet using Codeanywhere, simply go to File -> New Connection -> DigitalOcean.

![](/images/digitalocean-open.png)

After selecting DigitalOcean, Add DigitalOcean Access window appears. Click on "Connect your DigitalOcean Account" in order to proceed.

![](/images/digitalocean-connect.png)

Enter your Digital Ocean account details to log in and connect to your Digital Ocean account and authorize Codeanywhere for quick and easy access!

![](/images/digitalocean-authorize.png)

Now, in your Editor, you’ll be able to create a new Droplet which will be added to your Digital Ocean account.

### Creating a new Droplet
First of all, you can select your new Droplet image from 4 categories: Distributions, One-click Apps, Snapshots and Backups. Also, here, you can select Droplet’s Size, as well as Region of your Droplet - the same way you do that with Digital Ocean!

![](/images/do-droplet-create1.png)

After selecting Next, you can enter Host name of your Droplet which will also be shown in your Codeanywhere file tree, as well as in your Digital Ocean account, SSH Keys you’d like to import and any Additional Add-on you’d like to select.

![](/images/do-droplet-create2.png)

Click Create and your Droplet will be added into your Codeanywhere account and to your Digital Ocean account!

### Managing a Droplet

![](/images/do-droplet-manage.png)

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

![](/images/do-droplet-deleted.png)

Keep in mind, that if you use Codeanywhere to Remove your Droplet, it will disappear from your Codeanywhere account, but you’ll still be able to access it using Digital Ocean.

### Adding authorization to a different account
If you want to remove authorization for your Digital Ocean account, go to your Dashboard and under Account, select Disconnect from your current Digital Ocean account.

![](/images/do-droplet-dashboard.png)

Now, you can authorize different Digital Ocean account by simply Connecting to a different one - the same way as described before, or if you’re already logged in Digital Ocean account, directly from your Dashboard.

### Adding existing Droplet
While creating a Droplet via Codeanywhere, we have a full integration, and connection of an existing Droplet is possible by using SSH connection. While connecting via [SSH server](#sftp-ssh), you have to take your CA public key and implement it inside authenticated_keys.

## OneDrive

With Codeanywhere, you can connect your OneDrive account!

### Adding a New Connection to OneDrive
Go to File -> New Connections -> OneDrive.

![](/images/onedrive-open.png)

After selecting it, Add OneDrive Access window appears. Click on "Add your OneDrive Account" in order to proceed.

![](/images/onedrive-connect.png)

Enter your OneDrive account details to add that OneDrive account to your server list for quick and easy access.

![](/images/onedrive-login.png)

If the OneDrive account is added successfully it will appear in your File Explorer with the OneDrive icon. Now you can easily edit files from your OneDrive account!
