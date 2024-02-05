---
navigation:
  - splfileinfo.setinfoclass.md: '« SplFileInfo::setInfoClass'
  - class.splfileobject.md: SplFileObject »
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::\_\_function toString() { \[native code\] }

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::\_\_toString — Повертає шлях до файлу у вигляді рядка

### Опис

```methodsynopsis
public SplFileInfo::__toString(): string
```

Цей метод поверне ім'я цього файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу.

### Приклади

**Пример #1 Пример использования**SplFileInfo::\_\_toString()\*\*\*\*

```php
<?php
$info = new SplFileInfo('foo');
var_dump($info->__toString());
echo $info.PHP_EOL;

$info = new SplFileInfo('/usr/bin/php');
var_dump($info->__toString());
echo $info.PHP_EOL;
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(3) "foo"
foo
string(12) "/usr/bin/php"
/usr/bin/php
```
