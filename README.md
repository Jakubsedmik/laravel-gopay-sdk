# GoPay SDK for Laravel


  - [Installation](#installation)
    - [Step 1: Install package](#step-1-install-package)
    - [Step 2: Configuration](#step-2-configuration)
  - [Usage/Examples](#usageexamples)

## Installation

### Step 1: Install package

Add the package in your composer.json by executing the command:

```
composer require pavelzanek/laravel-gopay-sdk
```

This command installs the package into the vendor/ directory.

### Step 2: Configuration

You can initialise config file by running command:

```
php artisan vendor:publish --provider="PavelZanek\LaravelGoPaySDK\Providers\GoPayServiceProvider" --tag="config"
```

Next, you can see newly created file located in `config` folder - `gopay.php`. 

By default, the config file looks like this

```
<?php

return [
    'goid' => env('GOPAY_ID'),
    'clientId' => env('GOPAY_CLIENT_ID'),
    'clientSecret' => env('GOPAY_CLIENT_SECRET'),
    'defaultScope' => env('GOPAY_DEFAULT_SCOPE', 'ALL'),
    'gatewayUrl' => env('GOPAY_PRODUCTION_ENV', true) ? 
        'https://gate.gopay.cz/api/' : 'https://gw.sandbox.gopay.com/api/',
    'languages' => [ 
        'en' => 'ENGLISH',
        'sk' => 'SLOVAK',
        'cs' => 'CZECH'
    ],
    'timeout' => 30
];
```

Basic variables can be set in .env file.

## Usage/Examples

TODO