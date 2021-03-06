# ZipWhip-PHP-API [WIP]

[![Packagist](https://img.shields.io/packagist/dm/colling-media/zipwhip-php-api.svg?maxAge=2592000)](https://packagist.org/packages/colling-media/zipwhip-php-api)
[![Packagist](https://img.shields.io/packagist/dt/colling-media/zipwhip-php-api.svg?maxAge=2592000)](https://packagist.org/packages/colling-media/zipwhip-php-api)
[![Github All Releases](https://img.shields.io/github/downloads/Colling-Media/ZipWhip-PHP-API/total.svg?maxAge=2592000)](https://github.com/Colling-Media/ZipWhip-PHP-API)

Make sure you have a ZipWhip account! Visit [zipwhip.com](http://zipwhip.com) and register to get your username and password!

## Installation

`composer require colling-media/zipwhip-php-api`

## Getting Started

```php

$user = "YOUR_USERNAME_HERE"; //Typically, this is your phone number
$pass = "YOUR_PASSWORD_HERE";

$zipWhip = new \CollingMedia\ZipWhipClient($user, $pass);

$message = "Hello World";
$number = "5555555555"; //This can be an int too, either way works.

$zipWhip->sendMessage($number, $message); //Yay! Your message was sent, and you should be receiving it soon!

```

## Available Methods

`$zipWhip->deleteContact($contactId);`

`$zipWhip->listContacts();`

`$zipWhip->saveContact($contactInfo);`

*For contact info, it must be an array, follow [thier guide](https://www.zipwhip.com/api/curl/contact/save) to see what is allowed.

`$zipWhip->deleteConversation($fingerprint);`

`$zipWhip->getConversation($fingerprint, $limit, $start);`

`$zipWhip->listConversations($limit, $start);`

*NOTE!* I didn't get to finish added the methods, will add tomorrow.

Find any issues? Let us know, and we will fix them ASAP!
