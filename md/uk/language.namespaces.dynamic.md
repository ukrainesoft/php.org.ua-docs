Простори імен та динамічні особливості мови

-   [« Використання простору імен: основи](language.namespaces.basics.md)
    
-   [Ключевое слово namespace и константаNAMESPACE](language.namespaces.nsconstants.md)
    
-   [PHP Manual](index.md)
    
-   [Пространства имён](language.namespaces.md)
    
-   Простори імен та динамічні особливості мови
    

## Простори імен та динамічні особливості мови

(PHP 5> = 5.3.0, PHP 7, PHP 8)

На реалізацію просторів імен PHP вплинули і динамічні особливості мови. Перетворимо нижченаведений код для використання просторів імен:

**Приклад #1 Динамічно доступні елементи**

example1.php:

```php
<?php
class classname
{
    function __construct()
    {
        echo __METHOD__,"\n";
    }
}
function funcname()
{
    echo __FUNCTION__,"\n";
}
const constname = "global";

$a = 'classname';
$obj = new $a; // выводит classname::__construct
$b = 'funcname';
$b(); // выводит funcname
echo constant('constname'), "\n"; // выводит global
?>
```

Необхідно використати абсолютне ім'я (ім'я класу з префіксом простору імен). Зверніть увагу, що немає різниці між повним ім'ям і абсолютним всередині динамічного імені класу, функції або константи. Початковий зворотний сліш не є необхідним.

**Приклад #2 Динамічно доступні елементи простору імен**

```php
<?php
namespace namespacename;
class classname
{
    function __construct()
    {
        echo __METHOD__,"\n";
    }
}
function funcname()
{
    echo __FUNCTION__,"\n";
}
const constname = "namespaced";

include 'example1.php';

$a = 'classname';
$obj = new $a; // выводит classname::__construct
$b = 'funcname';
$b(); // выводит funcname
echo constant('constname'), "\n"; // выводит global

/* обратите внимание, что при использовании двойных кавычек символ обратного слеша должен быть заэкранирован. Например, "\\namespacename\\classname" */
$a = '\namespacename\classname';
$obj = new $a; // выводит namespacename\classname::__construct
$a = 'namespacename\classname';
$obj = new $a; // также выводит namespacename\classname::__construct
$b = 'namespacename\funcname';
$b(); // выводит namespacename\funcname
$b = '\namespacename\funcname';
$b(); // также выводит namespacename\funcname
echo constant('\namespacename\constname'), "\n"; // выводит namespaced
echo constant('namespacename\constname'), "\n"; // также выводит namespaced
?>
```

Обов'язково прочитайте [примітка про екранування імен простору імен у рядках](language.namespaces.faq.html#language.namespaces.faq.quote)