Отримує тип файлу

-   [« SplFileInfo::getSize](splfileinfo.getsize.html)
    
-   [SplFileInfo::isDir »](splfileinfo.isdir.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує тип файлу
    

# SplFileInfo::getType

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getType — Отримує тип файлу

### Опис

```methodsynopsis
public SplFileInfo::getType(): string|false
```

Повертає тип файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок (string), що представляє тип елемента. Можливі такі значення: `file` `link` `dir` `block` `fifo` `char` `socket` або `unknown`. У разі виникнення помилки повертає **`false`**

### Помилки

Викидає [RuntimeException](class.runtimeexception.html) у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getType()****

```php
<?php

$info = new SplFileInfo(__FILE__);
echo $info->getType().PHP_EOL;

$info = new SplFileInfo(dirname(__FILE__));
echo $info->getType();

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
file
dir
```