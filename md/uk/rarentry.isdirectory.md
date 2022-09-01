---
navigation:
  - rarentry.getversion.md: '« RarEntry::getVersion'
  - rarentry.isencrypted.md: 'RarEntry::isEncrypted »'
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::isDirectory'
---
# RarEntry::isDirectory

(PECL rar >= 2.0.0)

RarEntry::isDirectory — Перевіряє, чи є запис директорією

### Опис

```methodsynopsis
public RarEntry::isDirectory(): bool
```

Перевіряє, чи є поточний запис директорією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`** Залежно від результату.

### Примітки

Функція доступна з версії 2.0.0, а для попередніх версій можна перевіряти атрибути запису (Працює тільки для файлів, стислих у RAR для Windows або Unix):

```php
<?php
//...
//Откроем файл, получим запись и сохраним в переменной $e...
//...

$isDirectory = (bool) ((($e->getHostOs() == RAR_HOST_WIN32) && ($e->getAttr() & 0x10)) ||
    (($e->getHostOs() == RAR_HOST_UNIX) && (($e->getAttr() & 0xf000) == 0x4000)));
?>
```
