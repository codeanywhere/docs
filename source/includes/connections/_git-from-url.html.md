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
