Перевіряє, чи можна модифікувати phar-архів

-   [« Phar::isValidPharFilename](phar.isvalidpharfilename.html)
    
-   [Phar::loadPhar »](phar.loadphar.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Перевіряє, чи можна модифікувати phar-архів
    

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

Повертає **`true`**якщо архів можна модифікувати

### Дивіться також

-   [Phar::canWrite()](phar.canwrite.html) - Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
-   [PharData::isWritable()](phardata.iswritable.html) - Перевірити, чи можна модифікувати tar/zip-архів