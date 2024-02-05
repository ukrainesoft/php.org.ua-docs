---
navigation:
  - phardata.offsetunset.md: '« PharData::offsetUnset'
  - phardata.setdefaultstub.md: 'PharData::setDefaultStub »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::setAlias'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::setAlias

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::setAlias ​​— Функція заглушка (Phar::setAlias ​​не можна використовувати для PharData)

### Опис

```methodsynopsis
public PharData::setAlias(string $alias): bool
```

Незапускні tar/zip-архіви не можуть мати псевдоніма, тому цей метод просто викидає виняток.

### Список параметрів

`alias`

Параметр ігнорується.

### Значення, що повертаються

### Помилки

Викидає виняток [PharException](class.pharexception.md)

### Дивіться також

-   [Phar::setAlias()](phar.setalias.md) \- Встановити псевдонім для Phar-архіву
