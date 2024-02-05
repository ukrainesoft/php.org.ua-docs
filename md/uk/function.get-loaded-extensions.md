---
navigation:
  - function.get-included-files.md: « get\_included\_files
  - function.get-magic-quotes-gpc.md: get\_magic\_quotes\_gpc »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_loaded\_extensions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_loaded\_extensions

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_loaded\_extensions — Повертає масив імен усіх скомпілованих та завантажених модулів

### Опис

```methodsynopsis
get_loaded_extensions(bool $zend_extensions = false): array
```

Функція повертає масив імен усіх скомпільованих та завантажених в інтерпретаторі PHP модулів.

### Список параметрів

`zend_extensions`

Повернути тільки модулі Zend або звичайні модулі, такі як mysqli. За замовчуванням **`false`** (Повернення звичайних модулів).

### Значення, що повертаються

Повертає індексований масив імен усіх модулів.

### Приклади

**Пример #1 Пример использования**get\_loaded\_extensions()\*\*\*\*

```php
<?php
print_r(get_loaded_extensions());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Core
    [1] => date
    [2] => libxml
    [3] => pcre
    [4] => sqlite3
    [5] => zlib
    [6] => ctype
    [7] => dom
    [8] => fileinfo
    [9] => filter
    [10] => hash
    [11] => json
    [12] => mbstring
    [13] => SPL
    [14] => PDO
    [15] => session
    [16] => posix
    [17] => Reflection
    [18] => standard
    [19] => SimpleXML
    [20] => pdo_sqlite
    [21] => Phar
    [22] => tokenizer
    [23] => xml
    [24] => xmlreader
    [25] => xmlwriter
    [26] => gmp
    [27] => iconv
    [28] => intl
    [29] => bcmath
    [30] => sodium
    [31] => Zend OPcache
)
```

### Дивіться також

-   [get\_extension\_funcs()](function.get-extension-funcs.md) \- Повертає масив імен функцій модуля
-   [extension\_loaded()](function.extension-loaded.md) \- Визначає, чи завантажений модуль
-   [dl()](function.dl.md) \- Завантажує модуль PHP під час виконання
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
