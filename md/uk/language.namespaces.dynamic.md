---
navigation:
  - language.namespaces.basics.md: « Основи
  - language.namespaces.nsconstants.md: Ключове слово namespace та константа\_\_NAMESPACE\_\_ »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: Простори імен та динамічні особливості мови
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Простори імен та динамічні особливості мови

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

На реалізацію просторів імен PHP вплинули і динамічні властивості мови. Тому, щоб перетворити код на кшталт наступного прикладу на код, який буде працювати всередині простору імен:

**Приклад #1 Динамічно доступні елементи**

example1.php:

```php
<?php

class classname
{
    function __construct()
    {
        echo __METHOD__,"\n";
    }
}

function funcname()
{
    echo __FUNCTION__,"\n";
}

const constname = "global";

$a = 'classname';
$obj = new $a; // выводит classname::__construct
$b = 'funcname';
$b(); // выводит funcname
echo constant('constname'), "\n"; // выводит global

?>
```

Потрібно зазначити абсолютне ім'я (ім'я класу з префіксом простору імен). Зверніть увагу, оскільки між повним і абсолютним ім'ям усередині динамічного імені класу, функції чи константи немає різниці, початковий зворотний сліш не потрібен.

**Приклад #2 Динамічно доступні елементи простору імен**

```php
<?php

namespace namespacename;

class classname
{
    function __construct()
    {
        echo __METHOD__,"\n";
    }
}

function funcname()
{
    echo __FUNCTION__,"\n";
}

const constname = "namespaced";

include 'example1.php';

$a = 'classname';
$obj = new $a; // выводит classname::__construct
$b = 'funcname';
$b(); // выводит funcname
echo constant('constname'), "\n"; // выводит global

/* обратите внимание, что в двойных кавычках символ обратного слеша нужно заэкранировать. НаПриклад, "\\namespacename\\classname" */
$a = '\namespacename\classname';
$obj = new $a; // выводит namespacename\classname::__construct
$a = 'namespacename\classname';
$obj = new $a; // также выводит namespacename\classname::__construct
$b = 'namespacename\funcname';
$b(); // выводит namespacename\funcname
$b = '\namespacename\funcname';
$b(); // также выводит namespacename\funcname
echo constant('\namespacename\constname'), "\n"; // выводит namespaced
echo constant('namespacename\constname'), "\n"; // также выводит namespaced

?>
```

Обов'язково прочитайте [примітка про екранування імен простору імен у рядках](language.namespaces.faq.md#language.namespaces.faq.quote)
