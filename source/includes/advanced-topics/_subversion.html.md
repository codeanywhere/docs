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
