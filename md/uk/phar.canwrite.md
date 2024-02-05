---
navigation:
  - phar.cancompress.md: '« Phar::canCompress'
  - phar.compress.md: 'Phar::compress »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::canWrite'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::canWrite

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::canWrite — Перевіряє, чи підтримує модуль phar збереження та створення phar-архівів

### Опис

```methodsynopsis
final public static Phar::canWrite(): bool
```

Цей статичний метод визначає, чи було вимкнено доступ на запис у системному файлі php.ini з використанням змінної [phar.readonly](phar.configuration.md#ini.phar.readonly)

### Список параметрів

### Значення, що повертаються

**`true`**, якщо доступ до запису увімкнено, **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**Phar::canWrite()\*\*\*\*

```php
<?php
if (Phar::canWrite()) {
    file_put_contents('phar://myphar.phar/file.txt', 'всем привет');
}
?>
```

### Дивіться також

-   [phar.readonly](phar.configuration.md#ini.phar.readonly)
-   [Phar::isWritable()](phar.iswritable.md) \- Перевіряє, чи можна модифікувати phar-архів
