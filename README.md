#PHP encryptionClass

##Feature

This class offers a wrapper for the php5-mcrypt module that helps you encrypting and decrypting data. The encrypted data can be returned in binary or hexadecimal form.

##Installation

###Installing the extension

This class needs the `php5-mcrypt` module which is really easy to install via apt-get or aptitude:
```
sudo apt-get install php5-mcrypt
sudo apacht2ctl -k restart #if you use apache (you shouldn't ... use nginx!)
```
You're done! The php5 mcrypt module is installed and ready to be used.
If you have problems installing the module check out http://www.php.net/manual/en/mcrypt.setup.php

###Configuring the script

For real security **you should change the encryption key**!
You'll find it within the class file *encryption.class.php*.
```php
...
	CONST DEFAULT_KEY = 'e2bf5a831914c';
...
```

##Usage

just require the class file and start encrypting:
```php
<?
	require 'encryption.class.php';
	
	$string = Encryption::encrypt('encrypt me');
	echo $string; #should display "794af027bf97b9532b9ec0da3dffecc11d9a6a97b08a1775"
?>
```
Decrypting is as easy as encrypting:
```php
<?
	require 'encryption.class.php';
	
	$string = Encryption::decrypt('ec762103b818704154a5ee13bb641c935986d3e03991301f');
	echo $string; #should display "decrypt me"
?>
```

##Have fun!

Oh yeah! This class is for securing the data you are handling with on your site :)
