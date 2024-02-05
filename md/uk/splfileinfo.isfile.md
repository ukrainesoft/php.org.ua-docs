---
navigation:
  - splfileinfo.isexecutable.md: '« SplFileInfo::isExecutable'
  - splfileinfo.islink.md: 'SplFileInfo::isLink »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::isFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::isFile

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::isFile — Вказує, чи об'єкт посилається на звичайний файл

### Опис

```methodsynopsis
public SplFileInfo::isFile(): bool
```

Перевіряє, чи існує файл, на який посилається об'єкт SplFileInfo, і чи він є звичайним файлом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо файл існує і є звичайним файлом (а не посиланням), **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**SplFileInfo::isFile()\*\*\*\*

```php
<?php
$info = new SplFileInfo(__FILE__);
var_dump($info->isFile());

$info = new SplFileInfo(dirname(__FILE__));
var_dump($info->isFile());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```
