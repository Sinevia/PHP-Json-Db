# PHP-Json-Db

Easy to use key value storage, stored to a JSON file.
Great for prototyping.

## Usage ##

```php
// Initializing database, creating file if not existing
$db = new JsonDb('yourdb.json', true);

// Setting keys
$db->set('key1','Value of Key 1');
$db->set('key2','Value of Key 2');
$db->set('key3','Value of Key 3');

// Saving to database
$db->save();

// Getting keys
$key1 = $db->get('key1');
$key2 = $db->get('key2');
$key3 = $db->get('key3');

// Removing keys
$db->remove('key1');
$db->remove('key2');
$db->remove('key3');
$db->save();

// Deleting database
$db->delete();

// Check if database exists
if($db->exists()){
    echo 'Database ' . $db->filePath . ' exists';
} else {
    echo 'Database ' . $db->filePath . ' DOES NOT exist';
}

```
