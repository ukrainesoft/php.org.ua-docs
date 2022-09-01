---
navigation:
  - phar.decompressfiles.html: '« Phar::decompressFiles'
  - phar.delete.html: 'Phar::delete »'
  - index.html: PHP Manual
  - class.phar.html: Phar
title: 'Phar::delMetadata'
---
# Phar::delMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

Phar::delMetadata — Видалити глобальні метадані в архіві phar

### Опис

```methodsynopsis
public Phar::delMetadata(): bool
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Видаляє глобальні метадані в архіві phar

### Список параметрів

### Значення, що повертаються

Повертає **`true`** успішного виконання, але краще використовувати перевірку винятків.

### Помилки

Викидає виняток [PharException](class.pharexception.html) у разі виникнення помилки під час збереження змін на диск.

### Приклади

**Приклад #1 Приклад використання **Phar::delMetaData()****

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    var_dump($phar->getMetadata());
    $phar->setMetadata("hi there");
    var_dump($phar->getMetadata());
    $phar->delMetadata();
    var_dump($phar->getMetadata());
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

Результат виконання цього прикладу:

```
NULL
string(8) "hi there"
NULL
```

### Дивіться також

-   [Phar::getMetadata()](phar.getmetadata.html) - Витягти метадані phar-архіву
-   [Phar::setMetadata()](phar.setmetadata.html) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.html) - Перевірити, чи містить phar-архів глобальні метадані
