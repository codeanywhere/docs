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
