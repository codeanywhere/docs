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
