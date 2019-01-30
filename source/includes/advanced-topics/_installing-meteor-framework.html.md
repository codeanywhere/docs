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
