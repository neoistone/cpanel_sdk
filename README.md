# cpanel_sdk

### Creating Cpanel User ###
```
<?php
 include __DIR__.'/class.whm.php';
$WHM = new WHM( false , '1.1.1.1' , 'root' , 'pass' );
$domain = $_GET['domain'];
$email = $_GET['email'];
$package = $_GET['package'];

$data = array();
$data['domain'] = $domain;
$data['email'] = $email;
$data['package'] = $package;

print_r($WHM->create_account($data));
?>
```

### Creating User Ssesion ###
```
<?php
 include __DIR__.'/class.whm.php';
$WHM = new WHM( false , '1.1.1.1' , 'root' , 'pass' );
echo $WHM->login_with_user();
?>
```
#### RETURN login url ####