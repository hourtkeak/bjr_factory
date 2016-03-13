
     ,-----.,--.                  ,--. ,---.   ,--.,------.  ,------.
    '  .--./|  | ,---. ,--.,--. ,-|  || o   \  |  ||  .-.  \ |  .---'
    |  |    |  || .-. ||  ||  |' .-. |`..'  |  |  ||  |  \  :|  `--, 
    '  '--'\|  |' '-' ''  ''  '\ `-' | .'  /   |  ||  '--'  /|  `---.
     `-----'`--' `---'  `----'  `---'  `--'    `--'`-------' `------'
    ----------------------------------------------------------------- 


Hi there! Welcome to Cloud9 IDE!

To get you started, we have created a small hello world application.

1) Open the hello-world.php file

2) Follow the run instructions in the file's comments

3) If you want to look at the Apache logs, check out ~/lib/apache2/log

And that's all there is to it! Just have fun. Go ahead and edit the code, 
or add new files. It's all up to you! 

Happy coding!
The Cloud9 IDE team


## Support & Documentation

Visit http://docs.c9.io for support, or to learn more about using Cloud9 IDE. 
To watch some training videos, visit http://www.youtube.com/user/c9ide


rm README.md php.ini hello-world.php
sudo composer self-update
composer create-project laravel/laravel ./laravel --prefer-dist
shopt -s dotglob
mv laravel/* ./
rm -rf laravel
As Lavarel is serving its content from the public directory we need to modify the apache config using nano (a text editor):

sudo nano /etc/apache2/sites-enabled/001-cloud9.conf
Then do the following:

// Change this line
DocumentRoot /home/ubuntu/workspace

// To following
DocumentRoot /home/ubuntu/workspace/public
To save the file press F2, then 'Y' and 'Enter'.

Get the latest version of Laravel (i.e. 5.0.23 on the 29th March, 2015)

sudo composer update
Next you need to setup your database to work with Laravel - to do this, you first need to know the hostname, username and database name. The "mysql-ctl cli" command will give you these details

mysql-ctl cli
use c9;
select @@hostname;
exit
Edit the Laravel environment configuration file ".env" (in the root directory) and add the database settings

DB_HOST=localhost
DB_DATABASE=c9
DB_USERNAME=USERNAME
DB_PASSWORD=



https://community.c9.io/t/getting-started-with-laravel/1608