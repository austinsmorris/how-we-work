PHP
===

For all new php code, we strictly adhere to the [PSR-2](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md) standard, with the following additions:

###PHP Tags###

**There MUST be one blank line after the <code><?php</code> tag.**

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

**Properties and variables MUST be in <code>$lowerCamelCase</code>.**

Yes:
    $myPropertyName
    $yourVariableName
    $properties
    
No:
    $my_property_name
    $yourvariablename
    $Properties
    
**The purpose of a property or variable SHOULD be obvious.**

This simply means use human-readable variable names that make sense in the context of their usage.  We are writing maintainable code, not algebraic formulas.

Yes:
    $area = $height * width;
    
No:
    $z = $x + $y;
    
###Associative Array Keys###

**Associative array keys must me all lower-case and <code>underscore_separated</code>.**

This is the cleanest way to support json serialization in a way that is human-readable and supports the use of javascript dot notation when consumed by a client.  Therefore it shall be consistent in all code.

Yes:
    $foo['my_key_name'] = $bar;
    
No:
    $foo['yourKeyName'] = $bar;
    $foo['your-key-name'] = $bar;
    $foo['your key name'] = $bar;
    $foo['Keys'] = $bar;
    
