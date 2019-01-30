# Advanced Topics
## Changing MySQL password
Our [Containers](#container) created from stacks that include a MySQL database are preconfigured with a passwordless root account for ease of use. This is OK for the initial setup and development without any sensitive data. We strongly advise that you change your password and you can do it easily with the following commans in your terminal:

Login to your database:

~~~~
mysql -u root
~~~~

Execute the following commands in MySQL console:


```sql
SET PASSWORD FOR 'root'@'localhost' = PASSWORD('YourNewPassword');
exit

```

Now, you just login to your database with the new password in terminal or phpmyadmin:

~~~~
mysql -u root -p
~~~~

You will be prompted for the password after hitting Enter.

## Installing SASS
Sass is an extension of CSS that adds power and elegance to the basic language. It allows you to use variables, nested rules, mixins, inline imports, and more, all with a fully CSS-compatible syntax.

Our [Containers](#container) don't have SASS preinstalled, but you can set it up easily!

First of all, you'll have to create an Container. Of course, you can use any Stack but you'll have to install Ruby first. The recommended way is to use RVM. As a first step install mpapis public key used to verify installation package to ensure security.:

~~~~
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
~~~~

Install RVM stable with ruby:

~~~~
curl -sSL https://get.rvm.io | bash -s stable --ruby
~~~~

Now you may load RVM with the following command:

~~~~
source ~/.rvm/scripts/rvm
~~~~

Now, you just have to install the Sass gem with the following command:

~~~~
gem install sass
~~~~

You can use the command line to run Sass:

~~~~
sass input.scss output.css
~~~~

## Installing Laravel framework
[Containers](#container) created from our PHP stack come with all the requirements for the Laravel framework preinstalled and properly configured. Laravel utilizes Composer to manage its dependencies so it is a matter of running few commands to get a working Laravel installation. First, download the Laravel installer using Composer in your terminal:

~~~~
composer global require "laravel/installer"
~~~~

Once installed, the `laravel new` command will create a fresh Laravel installation in the `workspace` directory.

~~~~
cd ~/workspace
laravel new
~~~~

Now you just need to configure permissions of the `storage` and the `bootstrap/cache` directories which should be writable by your web server.

~~~~
chmod -R ug+rwx storage bootstrap/cache
~~~~

### Public Directory
`workspace` folder is your Document Root and Laravel's `public` directory serves as the front controller for all HTTP requests entering your application. If you would like to remove `/public` from your preview URL, just create a file named `.htaccess` in your `workspace` and save the following in it:

~~~~
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteRule ^(.*)$ public/$1 [L]
</IfModule>
~~~~

## Installing Angular framework
In order to install Angular framework, first create a [Container](#container) with the Node.js stack. Node.js has it's own package manager `npm` with whom you will install the Angular CLI.

~~~~
npm install -g @angular/cli
~~~~

Now that you have the Angular CLI installed, create a new project in your `workspace`:

~~~~
cd ~
ng new workspace 
~~~~

After the project is created, go to the project directory and launch the server:

~~~~
cd ~/workspace
ng serve --host 0.0.0.0 --port 3000
~~~~

Once launched, you can preview your application with your container preview URL.

## Installing Django framework
In order to install Django framework, first create a [Container](#container) with the Python stack. Python has it's own package manager pip with whom you will install the Django framework.

~~~~
pip install Django
~~~~

Now that you have Django installed, create a new project in your `workspace`:

~~~~
cd ~/workspace
django-admin startproject app
~~~~

After the project is created, go to the project directory and launch the server:

~~~~
cd ~/workspace/app
python manage.py runserver 0.0.0.0:3000
~~~~

Once launched, you can preview your application with your container preview URL.

## Installing Meteor Framework
_NOTE: Meteor is resource intensive. Minimal system requirement for a succesfull application initialization is 512MB of RAM and 3GB of disk space._

To install Meteor framework on a Codeanywhere [container](#container), just run the following command in your terminal to install the latest official Meteor release:

~~~~
curl https://install.meteor.com/ | sh
~~~~

Once installed, the `meteor create` command will create a fresh Laravel installation in the `workspace` directory.

~~~~
cd ~/workspace
meteor create .
~~~~

Now you can run your Meteor app by running:

~~~~
meteor run
~~~~

and previewing it on your preview URL after the app is lifted.

## Installing MongoDB

### Ubuntu 16.04
To install mongoDB on a Codeanywhere [container](#container) based on Ubuntu 16.04 distribution, just run the followings commands in your terminal to install the latest official MongoDB release:

Import the public key used by the package management system.

~~~~
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB49F368818C72E52529D4
~~~~

Create a `/etc/apt/sources.list.d/mongodb-enterprise.list` file for MongoDB.

~~~~
echo "deb [ arch=amd64,arm64,ppc64el,s390x ] http://repo.mongodb.com/apt/ubuntu xenial/mongodb-enterprise/4.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-enterprise.list
~~~~

Reload local package database and install the MongoDB Enterprise packages.

~~~~
sudo apt-get update
sudo apt-get install -y mongodb-enterprise
~~~~

Start MongoDB

~~~~
sudo systemctl mongod start
~~~~

### CentOS 7.2

To install mongoDB on a Codeanywhere [container](#container) based on CentOS 7.2 distribution, just run the followings commands in your terminal to install the latest official MongoDB release:

Configure repository with the `vim` editor:
~~~~
sudo vim /etc/yum.repos.d/mongodb-enterprise.repo
~~~~

Put the following contents in the file:

~~~~
[mongodb-enterprise]
name=MongoDB Enterprise Repository
baseurl=https://repo.mongodb.com/yum/redhat/$releasever/mongodb-enterprise/4.0/$basearch/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.0.asc
~~~~

Install the MongoDB Enterprise packages

~~~~
sudo yum install -y mongodb-enterprise
~~~~

Start and enable MongoDB on startup

~~~~
sudo systemctl start mongod
sudo systemctl enable mongod
~~~~

## Installing MEAN Stack
In order to install MEAN stack, create a [Container](#container) with the Node.js stack. First you will now need to install MongoDB, check the following [guide](#installing-mongodb).

Now that you have MongoDB installed, clone the MEAN repo in your `workspace`:

~~~~
git clone https://github.com/linnovate/mean.git ~/workspace
~~~~

Now you need to set an example environment file and install the dependencies

~~~~
mv .env.example .env
yarn install
~~~~

Finally build the app and serve it on port 3000 and you should be able to preview it when it successfully runs all commands

~~~~
yarn build
SERVER_PORT=3000 yarn start
~~~~

## Working with repositories
With Codeanywhere, you’ll be able to work directly with your repositories. You can work with your resository using standard git commands inside your SSH terminal. Right click on your Container and select SSH Terminal in order to open it up.

### Setting up a Repository
Create a new local repository:

~~~~
git init
~~~~

Create a new repository out of a directory:

~~~~
git init <directory> 
~~~~

Create a copy of an existing repository inside Container:

~~~~
git clone /path/repository_name.git 
~~~~

Create a copy of an existing repository inside Container into an directory:

~~~~
git clone /path/repository_name.git <directory>  
~~~~

Create a copy of an private repository inside Container:

~~~~
git clone username@host:/path/repository_name.git 
~~~~

### Saving changes
Stage all changes in a file for next commit:

~~~~
git add <filename> 
~~~~

Stage all changes in a folder for next commit:

~~~~
git add <foldername> 
~~~~

Add all files to staging:

~~~~
git add * 
~~~~

Commit changes to head:

~~~~
git commit -m "Commit message" 
~~~~

Commit all changes in the working directory:

~~~~
git commit -a 
~~~~

### Inspecting a Repository
List which files are staged, unstaged, and untracked:

~~~~
git status 
~~~~

Display the entire commit history using the default formatting:

~~~~
git log 
~~~~

### Connecting to a remote Repository
Add the server to be able to push to it:

~~~~
git remote add origin <server> 
~~~~

List all currently configured remote repositories:

~~~~
git remote -v 
~~~~

### Working with branches

Create a new branch and switch to it:

~~~~
git checkout -b <branchname>
~~~~

Switch from one branch to another:

~~~~
git checkout <branchname> 
~~~~

List all the branches in your repo, and also tell you what branch you're currently in:

~~~~
git branch 
~~~~

Delete the feature branch:

~~~~
git branch -d <branchname> 
~~~~

Push the branch to your remote repository, so others can use it:

~~~~
git push origin <branchname> 
~~~~

Push all branches to your remote repository:

~~~~
git push --all origin 
~~~~

Delete a branch on your remote repository:

~~~~
git push origin :<branchname> 
~~~~

For example, if you want to push to your master branch, just use:

~~~~
git push origin master 
~~~~

### Update to a remote repository

Merge changes on the remote server to your Container:

~~~~
git pull 
~~~~

Merge a different branch into your active branch:

~~~~
git merge <branchname> 
~~~~

View all the merge conflicts

~~~~
git diff 
~~~~

## Changing document root in container
### .htaccess
CWD (curent working directory) - inside your Config file - is the location in which your run commands should be located. The default location is ~/workspace, if your commands are located in a subdirectory named "test” then cwd should be ~/workspace/test.

Apache installed on containers by default usually point to the workspace directory for the root of the website. If you need it to point elsewhere create or edit the .htaccess file located in the workspace directory. Here are the instructions for you:

~~~~
vim .htaccess 
~~~~

~~~~
<IfModule mod_rewrite.c> 
RewriteEngine on 
RewriteRule ^(.*)$ directory-name/$1 [L] 
</IfModule>
~~~~

The directory “directory-name” should be a subdirectory of workspace. Example: ~/workspace/test/test2/last-try/index.html RewriteRule ^(.*)$ test/test2/last-try/$1 [L]

## Subversion

Subversion is an open source version control system.

Codeanywhere doesn't have this feature yet. But you can set everything up using your Container's SSH Terminal.

### Ubuntu

Create a new [Container](#container) with Ubuntu.

In your SSH Terminal type in:

~~~~
sudo apt-get update
~~~~

in order to make sure that everything is up-to-date.

To install Subversion, run the following command from a terminal prompt:

~~~~
sudo apt-get install subversion apache2 libapache2-svn
~~~~

### CentOS

Create a new [Container](#container) with CentOS.

You don't have to update CentOS so you can install svn directly inside your container. Just run:

~~~~
yum install mod_dav_svn subversion
~~~~

### Configure Server
After you've installed packages on your Container, you can create a Subversion repository and access the project.

The Subversion repository can be created using the following command from a SSH terminal:

~~~~
svnadmin create /path/to/repo/
~~~~

Once you create the repository you can import files into the repository, just enter the following from a terminal prompt:

~~~~
svn import /path/to/directory path/to/repo/
~~~~
