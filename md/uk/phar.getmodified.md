---
navigation:
  - phar.getmetadata.md: '« Phar::getMetadata'
  - phar.getpath.md: 'Phar::getPath »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::getModified'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::getModified

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::getModified — Визначити, чи змінювався phar-архів

### Опис

```methodsynopsis
public Phar::getModified(): bool
```

Цей метод використовується для визначення, чи щось змінювалося в phar-архіві.

### Список параметрів

Без параметрів.

### Значення, що повертаються

**`true`**, якщо архів після відкриття змінювався та **`false`**, в іншому випадку.
