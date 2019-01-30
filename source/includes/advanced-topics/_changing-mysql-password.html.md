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
