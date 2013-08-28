# CodeIgniter Helper: CSV Export

**ci-csv**

## About this library

This CodeIgniter's Helper is used to create a CSV file in real time and then download it.

Its usage is recommended for CodeIgniter 2 or greater.

## Usage

```php
$this->load->helper('export_csv');

$fields = array(
    'id'   => 'ID',
    'name' => 'Name',
    'age'  => 'Age'
);

// the info inside $query is usually the response of a database query from a model
// an example of how to use this is calling a model method like: $query = $this->People->exportUsers();
// the following is just an example
$query = array();

$query[] = array(
    'id'   => 1,
    'name' => 'Ale Mohamad',
    'age'  => 29
);

$query[] = array(
    'id'   => 2,
    'name' => 'John Doe',
    'age'  => 36
);

echo arrayToCSV($query, $fields, "People");
```

![Ale Mohamad](http://alemohamad.com/github/logo2012am.png)