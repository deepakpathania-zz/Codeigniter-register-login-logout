# Codeigniter-register-login-logout
A user registration, login, logout system for Codeigniter 3.

# Quick Start
- First of all, clone this repo and save it's contents in your server folder, for example, if you'll be running this on localhost and you are using a linux environment, save it in <code>/var/www/html/login</code>. login is the name of the folder you will be placing the contents of this repo in.

- Now create a database and a table to store the user data.
```sql
create database login;
CREATE TABLE IF NOT EXISTS `user_login` (
`id` int(11) NOT NULL AUTO_INCREMENT,
`user_name` varchar(255) NOT NULL,
`user_email` varchar(255) NOT NULL,
`user_password` varchar(255) NOT NULL,
PRIMARY KEY (`id`)
);
```
- Now change the config file in the <code>config/config.php</code> file to modify the base url. If you named your folder login, the 26th line of config.php should look like <code>$config['base_url'] = 'http://localhost/login/';</code>

- In the <code>config/database.php</code> file, change the database details to point to your database by specifying the username, password and database name. The 76th line of database.php should look like
```sql
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
```
The username is generally root if you haven't changed it.

- Now go to <code>http://localhost/login/</code> to see your login system in action.
