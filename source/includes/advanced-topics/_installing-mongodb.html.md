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
sudo systemctl start mongod
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
