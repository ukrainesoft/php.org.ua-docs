---
navigation:
  - splfileinfo.getsize.md: '« SplFileInfo::getSize'
  - splfileinfo.isdir.md: 'SplFileInfo::isDir »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getType

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getType — Отримує тип файлу

### Опис

```methodsynopsis
public SplFileInfo::getType(): string|false
```

Повертає тип файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок (string), що представляє тип елемента. Можливі такі значення: `file` `link` `dir` `block` `fifo` `char` `socket`или`unknown`. У разі виникнення помилки повертає **`false`**

### Помилки

Викидає [RuntimeException](class.runtimeexception.md)в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getType()\*\*\*\*

```php
<?php

$info = new SplFileInfo(__FILE__);
echo $info->getType().PHP_EOL;

$info = new SplFileInfo(dirname(__FILE__));
echo $info->getType();

?>
```

Висновок наведеного прикладу буде схожим на:

```
file
dir
```
