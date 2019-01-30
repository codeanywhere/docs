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
