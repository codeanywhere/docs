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
