# Get it started.

In this chapter we are going to talk about the most common task: purchase of a product using [Payex](http://www.payexpim.com/).
We assume you already read [get it started](https://github.com/Payum/Core/blob/master/Resources/docs/get-it-started.md) from core.
Here we just show you modifications you have to put to the files shown there.

## Installation

The preferred way to install the library is using [composer](http://getcomposer.org/).
Run composer require to add dependencies to _composer.json_:

```bash
php composer.phar require payum/payex
```

## config.php

We have to only add the gateway factory. All the rest remain the same:

```php
<?php
//config.php

// ...

$factory = new \Payum\Payex\PayexGatewayFactory();
$gateways['payex'] = $factory->create(array(
    'account_number' => 'REPLACE IT',
    'encryption_key' => 'REPLACE IT',
    'sandbox' => true
));
```

## prepare.php

Here you have to modify a `gatewayName` value. Set it to `payex`. The rest remain the same as described basic [get it started](https://github.com/Payum/Core/blob/master/Resources/docs/get-it-started.md) documentation.

## Next 

* [Core's Get it started](https://github.com/Payum/Core/blob/master/Resources/docs/get-it-started.md).
* [The architecture](https://github.com/Payum/Core/blob/master/Resources/docs/the-architecture.md).
* [Supported gateways](https://github.com/Payum/Core/blob/master/Resources/docs/supported-gateways.md).
* [Storages](https://github.com/Payum/Core/blob/master/Resources/docs/storages.md).
* [Capture script](https://github.com/Payum/Core/blob/master/Resources/docs/capture-script.md).
* [Authorize script](https://github.com/Payum/Core/blob/master/Resources/docs/authorize-script.md).
* [Done script](https://github.com/Payum/Core/blob/master/Resources/docs/done-script.md).

Back to [index](index.md).