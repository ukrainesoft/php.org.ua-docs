Перевірити, чи можна модифікувати tar/zip-архів

-   [« PharData::extractTo](phardata.extractto.html)
    
-   [PharData::offsetSet »](phardata.offsetset.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Перевірити, чи можна модифікувати tar/zip-архів
    

# PharData::isWritable

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::isWritable — Перевірити, чи можна модифікувати tar/zip-архів

### Опис

```methodsynopsis
public PharData::isWritable(): bool
```

Цей метод повертає \*\*`true`\*\*якщо tar/zip-архів існує і доступний для запису. На відміну від [Phar::isWritable()](phar.iswritable.html), tar/zip-архіви з даними можна змінювати навіть якщо `phar.readonly` встановлений в `1`

### Список параметрів

Параметри відсутні.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### Дивіться також

-   [Phar::canWrite()](phar.canwrite.html) - Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
-   [Phar::isWritable()](phar.iswritable.html) - Перевіряє, чи можна модифікувати phar-архів