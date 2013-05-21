ZfrPusherModule
===============

[![Build Status](https://travis-ci.org/zf-fr/zfr-pusher-module.png?branch=master)](https://travis-ci.org/zf-fr/zfr-pusher-module) Version 1.0.0

Introduction
------------

ZfrPusherModule is a Zend Framework 2 module that integrates with [ZfrPusher](https://github.com/zf-fr/zfr-pusher)

Requirements
------------
* PHP 5.3
* [Zend Framework 2](https://github.com/zendframework/zf2)
* [ZfrPusher](https://github.com/zf-fr/zfr-pusher)

Installation
------------

Add "zfr/zfr-pusher-module" to your composer.json file and update your dependencies:

```
{
    "require": {
        "zfr/zfr-pusher-module": "1.*"
    }
}
```

Enable ZfrPusherModule in your `application.config.php`, then copy-paste the file `zfr_pusher.local.php.dist` (that
you can find in the `config` folder of the module) to your `autoload` folder (don't forget to remove the .dist at
the end!).

Usage
-----

The module registers the PusherClient and PusherService to the ZF 2 service manager. You can therefore get them like
this:

```php
// If you want to client:
$pusherClient = $serviceManager->get('ZfrPusher\Client\PusherClient');

// If you want the service:
$pusherService = $serviceManager->get('ZfrPusher\Service\PusherService');
```

For more information, please refer to the documentation of ZfrPusher to how to use them.
