---
navigation:
  - splfileinfo.isdir.md: '« SplFileInfo::isDir'
  - splfileinfo.isfile.md: 'SplFileInfo::isFile »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::isExecutable'
---
# SplFileInfo::isExecutable

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::isExecutable — Вказує, чи файл виконується.

### Опис

```methodsynopsis
public SplFileInfo::isExecutable(): bool
```

Перевіряє, чи файл виконуваний.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо файл виконується; **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::isExecutable()****

```php
<?php
$info = new SplFileInfo('/usr/bin/php');
var_dump($info->isExecutable());

$info = new SplFileInfo('/usr/bin');
var_dump($info->isExecutable());

$info = new SplFileInfo('foo');
var_dump($info->isExecutable());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
bool(false)
```
