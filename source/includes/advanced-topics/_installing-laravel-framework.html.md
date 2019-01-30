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
