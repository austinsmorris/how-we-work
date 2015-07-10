PHP
===

For all new php code, we strictly adhere to the [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) standard, with the following additions:

###PHP Tags###

**There MUST be one blank line after the **`<?php`** tag.**

Yes:

```php
<?php

namespace Vnn\Code;

use Bar;

class Foo extends Bar
{
// ...
```

No:

```php
<?php
namespace Vnn\Code;

use Bar;

class Foo extends Bar
{
// ...
```

```php
<?php
// I am a comment
namespace Vnn\Code;

use Bar;

class Foo extends Bar
{
// ...
```

###Properties and Variables###

**Properties and variables MUST be in **`$lowerCamelCase`**.**

Yes:
```php
$myPropertyName = $foo;
$yourVariableName = $foo;
$properties = $foo;
```
    
No:
```php
$my_property_name = $foo;
$yourvariablename = $foo;
$Properties = $foo;
```
    
**The purpose of a property or variable SHOULD be obvious.**

This simply means use human-readable variable names that make sense in the context of their usage.  We are writing maintainable code, not algebraic formulas.

Yes:
```php
$area = $height * width;
```
    
No:
```php
$z = $x + $y;
```
  
###Associative Array Keys###

**Associative array keys must me all lower-case and **`'underscore_separated'`**.**

This is the cleanest way to support json serialization in a way that is human-readable and supports the use of javascript dot notation when consumed by a client.  Therefore it shall be consistent in all code.

Yes:
```php
$foo['my_key_name'] = $bar;
```
  
No:
```php
$foo['yourKeyName'] = $bar;
$foo['your-key-name'] = $bar;
$foo['your key name'] = $bar;
$foo['Keys'] = $bar;
```
