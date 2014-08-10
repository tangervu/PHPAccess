PHPAccess
=========

Read Microsoft Access databases on Linux using mdbtools command line tools.

Installation
------------
The recommended way to install Connection.php is through [Composer](http://getcomposer.org).
```json
{
	"require": {
		"tangervu/phpaccess": "dev-master"
	}
}
```

Example
-------

```php
<?php
require('vendor/autoload.php'); //Use composer autoload

$access = new PHPAccess\PHPAccess('file.mdb');

//Get tables in access database
$tables = $access->getTables();

//Display contents of the tables
foreach($tables as $table) {
	print_r($access->getData($table));
}

//Export table structures as SQL queries
echo $access->getDatabaseSql('mysql');

//etc...

```
