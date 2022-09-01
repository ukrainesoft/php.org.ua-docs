---
navigation:
  - splfileinfo.islink.html: '« SplFileInfo::isLink'
  - splfileinfo.iswritable.html: 'SplFileInfo::isWritable »'
  - index.html: PHP Manual
  - class.splfileinfo.html: SplFileInfo
title: 'SplFileInfo::isReadable'
---
# SplFileInfo::isReadable

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::isReadable — Вказує, чи є файл доступним для читання

### Опис

```methodsynopsis
public SplFileInfo::isReadable(): bool
```

Перевіряє, чи файл доступний для читання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл доступний для читання; **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::isReadable()****

```php
<?php
$info = new SplFileInfo(__FILE__);
var_dump($info->isReadable());

$info = new SplFileInfo('foo');
var_dump($info->isReadable());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```
