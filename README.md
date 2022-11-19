# php-abi

PHP Ethereum ABI Encoder/Decoder

# Install


Then
```
composer require lessmore92/php-abi
```

# Usage

## Encode

```php
use Web3\Contracts\Ethabi;
use Web3\Contracts\Types\Address;
use Web3\Contracts\Types\Boolean;
use Web3\Contracts\Types\Bytes;
use Web3\Contracts\Types\DynamicBytes;
use Web3\Contracts\Types\Integer;
use Web3\Contracts\Types\Str;
use Web3\Contracts\Types\Uinteger;

$abi = new Ethabi([
    'address' => new Address(),
    'bool' => new Boolean(),
    'bytes' => new Bytes(),
    'dynamicBytes' => new DynamicBytes(),
    'int' => new Integer(),
    'string' => new Str(),
    'uint' => new Uinteger(),
]);

$abi->decodeParameter('uint', '0x0000000000000000000000000000000000000000000000000000000000000001');
// 1
$abi->decodeParameter('address', '0x0000000000000000000000000000000000000001');
// '0x0000000000000000000000000000000000000001'
```

# License
MIT
