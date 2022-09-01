---
navigation:
  - phar.isvalidpharfilename.md: '« Phar::isValidPharFilename'
  - phar.loadphar.md: 'Phar::loadPhar »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::isWritable'
---
# Phar::isWritable

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::isWritable — Перевіряє, чи можна модифікувати phar-архів

### Опис

```methodsynopsis
public Phar::isWritable(): bool
```

Цей метод повертає **`true`**, якщо `phar.readonly` встановлений в `0`архів існує і доступний для запису.

### Список параметрів

Параметрів немає.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо архів можна модифікувати

### Дивіться також

-   [Phar::canWrite()](phar.canwrite.md) - Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
-   [PharData::isWritable()](phardata.iswritable.md) - Перевірити, чи можна модифікувати tar/zip-архів
