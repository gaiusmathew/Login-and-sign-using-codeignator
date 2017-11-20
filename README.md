# codeignator-login-and-signup-
Shows how to create login and signup using codeignator

A user registration, login, logout system for Codeigniter 3.
Quick Start

    First of all, clone this repo and save it's contents in your server folder, for example, if you'll be running this on localhost and you are using a linux environment, save it in /var/www/html/login. login is the name of the folder you will be placing the contents of this repo in.

Now create a database and a table to store the user data.

create database login;
CREATE TABLE IF NOT EXISTS `user_login` (
`id` int(11) NOT NULL AUTO_INCREMENT,
`user_name` varchar(255) NOT NULL,
`user_email` varchar(255) NOT NULL,                             //note: if you have already created a table avoid first line query
`user_password` varchar(255) NOT NULL,
PRIMARY KEY (`id`)
);

                      

Now change the config file in the config/config.php file to modify the base url. If you named your folder login, the 26th line of config.php should look like $config['base_url'] = 'http://localhost/login/';

    In the config/database.php file, change the database details to point to your database by specifying the username, password and database name. The 76th line of database.php should look like

$db['default'] = array(
	'dsn'	=> '',
	'hostname' => 'localhost',
	'username' => 'your_username', 
	'password' => 'your_password',
	'database' => 'login',
	'dbdriver' => 'mysqli',
	'dbprefix' => '',
	'pconnect' => FALSE,
	'db_debug' => (ENVIRONMENT !== 'production'),
	'cache_on' => FALSE,
	'cachedir' => '',
	'char_set' => 'utf8',
	'dbcollat' => 'utf8_general_ci',
	'swap_pre' => '',
	'encrypt' => FALSE,
	'compress' => FALSE,
	'stricton' => FALSE,
	'failover' => array(),
	'save_queries' => TRUE
);

                                                          //note:The username is generally root if you haven't changed it.

    Now go to http://localhost/login/ to see your login system in action.
