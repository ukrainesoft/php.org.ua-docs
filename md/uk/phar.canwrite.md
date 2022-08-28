Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів

-   [« Phar::canCompress](phar.cancompress.html)
    
-   [Phar::compress »](phar.compress.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів
    

# Phar::canWrite

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::canWrite — Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів

### Опис

```methodsynopsis
final public static Phar::canWrite(): bool
```

Цей статичний метод визначає, чи було вимкнено доступ на запис у системному файлі php.ini з використанням змінної [phar.readonly](phar.configuration.html#ini.phar.readonly)

### Список параметрів

### Значення, що повертаються

**`true`**, якщо доступ до запису увімкнено, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **Phar::canWrite()****

```php
<?php
if (Phar::canWrite()) {
    file_put_contents('phar://myphar.phar/file.txt', 'всем привет');
}
?>
```

### Дивіться також

-   [phar.readonly](phar.configuration.html#ini.phar.readonly)
-   [Phar::isWritable()](phar.iswritable.html) - Перевіряє, чи можна модифікувати phar-архів