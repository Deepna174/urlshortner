# Build a URL shortener

Coverting an big url to a short url

Coded in PHP 
OS:Linux Ubuntu 18.04
webserver:Apache2
PHP version <=7.3.33
Mysql version <=5.7.37
IDE netbeans 10.0


## Step 1
unzip the shorturl.zip
Put the 'shorturl' into the web server root folder,
grant permission to the folder.

### LAMP '/var/www/html/'
### WAMP 'wamp/www'
### XAMP-'/opt/lampp/htdocs/'

## Step 2
import sql file 'shorturl/db_dump/shorturl.sql 

OR

Create a Database 'shorturl'

Table structure for table `shroten_url` 

CREATE TABLE `shroten_url` (
  `id` int(150) NOT NULL,
  `url` text NOT NULL,
  `short_code` text NOT NULL,
  `visit` int(150) NOT NULL DEFAULT '0',
  `added_on` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `updated_on` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

ALTER TABLE `shroten_url`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `shroten_url`
  MODIFY `id` int(150) NOT NULL AUTO_INCREMENT;

## Step3

open 'shorturl' project folder,config.php file update configuration of the database.Set hostname,username,password and database and base url 

## Step4
 access the project with your domain url example 'http://localhost/shorturl'

##Files included

### config.php -Configuration details are present in it aslomysql database connection
### header.php -jquery library and bootstrap cdn loaded here.
### footer.php.
### index.php- Landing page/home page
### short.php-To get the short code
### add.php- to add the short code
### shorturl.php- all database operations 
### README.md
### db_dump/shorturl.sql the sql file
