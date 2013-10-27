PHPAccess
=========

Read Microsoft Access databases on Linux using mdbtools command line tools.


Example
-------

```php
<?php
require 'PHPAccess.php'
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
