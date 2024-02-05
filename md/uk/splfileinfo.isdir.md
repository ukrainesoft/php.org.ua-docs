---
navigation:
  - splfileinfo.gettype.md: '« SplFileInfo::getType'
  - splfileinfo.isexecutable.md: 'SplFileInfo::isExecutable »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::isDir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::isDir

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::isDir — Вказує, чи є файл каталогом

### Опис

```methodsynopsis
public SplFileInfo::isDir(): bool
```

Цей метод можна використовувати для визначення того, чи файл каталогом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если каталог;**`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::isDir()\*\*\*\*

```php
<?php
$d = new SplFileInfo(dirname(__FILE__));
var_dump($d->isDir());

$d = new SplFileInfo(__FILE__);
var_dump($d->isDir());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```
