RestClient.PHP
==============

Simple REST client written in PHP and released under the MIT License

Example
=======
```php
<?php
    require_once('RestClient.php');
    
    $client = new RestClient();
    $result = $client->HTTP('http://www.example.com/my-user-endpoint', 
                             array( 'user_id' => '12388822',
                                    'fields' => 'name,age',
                                    'access_token' => 'aeb342cdab33b342cdab5ece335eb342cdabce6cbe' ),
                            'GET');
    echo "Server answered: \r\n";
    echo "HTTP Code: " . $result['Code'] . ", Body: " . $result['Response'] . "\r\n";
    echo "Headers: \r\n";
    foreach( $result['Headers'] as $name => $value ) {
        echo $name . ": " . $value . "\r\n";
    }
```
