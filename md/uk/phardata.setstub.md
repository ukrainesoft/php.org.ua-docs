---
navigation:
  - phardata.setsignaturealgorithm.md: '« PharData::setSignatureAlgorithm'
  - class.pharfileinfo.md: PharFileInfo »
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::setStub'
---
# PharData::setStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::setStub — Функція заглушка (Phar::setStub не можна використовувати для PharData)

### Опис

```methodsynopsis
public PharData::setStub(string $stub, int $len = -1): bool
```

tar/zip-архіви, що не запускаються, не можуть мати завантажувача (stub), так що цей метод просто кидає виняток.

### Список параметрів

`stub`

Параметр ігнорується.

`len`

Параметр ігнорується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [PharException](class.pharexception.md)

### Дивіться також

-   [Phar::setStub()](phar.setstub.md) - Встановити завантажувач або завантажувальну заглушку в Phar-архів
