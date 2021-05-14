# Helper class to create PSR-7 server request

A helper class that can create ANY PSR-7 server request.

## Installation

```bash
composer require terablaze/psr7-server
```

## Usage

```php
// Instanciate ANY PSR-17 factory implementations. Here is terablaze/psr7 as an example
$psr17Factory = new \TeraBlaze\Psr7\Factory\Psr17Factory();

$creator = new \TeraBlaze\Psr7Server\ServerRequestCreator(
    $psr17Factory, // ServerRequestFactory
    $psr17Factory, // UriFactory
    $psr17Factory, // UploadedFileFactory
    $psr17Factory  // StreamFactory
);

$serverRequest = $creator->fromGlobals();
```

## Other packages

* [terablaze/psr7](https://github.com/terablaze/psr7) - A super fast PSR-7 implementation.
* [laminas/laminas-httphandlerrunner](https://github.com/laminas/laminas-httphandlerrunner) - To send/emit PSR-7 responses
