---
navigation:
  - phardata.extractto.md: '« PharData::extractTo'
  - phardata.offsetset.md: 'PharData::offsetSet »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::isWritable'
---
# PharData::isWritable

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::isWritable — Перевірити, чи можна модифікувати tar/zip-архів

### Опис

```methodsynopsis
public PharData::isWritable(): bool
```

Цей метод повертає \*\*`true`\*\*якщо tar/zip-архів існує і доступний для запису. На відміну від [Phar::isWritable()](phar.iswritable.md), tar/zip-архіви з даними можна змінювати навіть якщо `phar.readonly` встановлений в `1`

### Список параметрів

Параметри відсутні.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### Дивіться також

-   [Phar::canWrite()](phar.canwrite.md) - Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
-   [Phar::isWritable()](phar.iswritable.md) - Перевіряє, чи можна модифікувати phar-архів
