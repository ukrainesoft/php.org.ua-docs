---
navigation:
  - phardata.decompressfiles.md: '« PharData::decompressFiles'
  - phardata.delete.md: 'PharData::delete »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::delMetadata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::delMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::delMetadata — Видалити глобальні метадані для zip-архіву

### Опис

```methodsynopsis
public PharData::delMetadata(): bool
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Видаляє глобальні метадані для zip-архіву

### Список параметрів

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, але краще використовувати перевірку винятків.

### Помилки

Викидає виняток [PharException](class.pharexception.md)в случае возникновения ошибки при сохранении изменений на диск.

### Приклади

**Пример #1 Пример использования**PharData::delMetaData()\*\*\*\*

```php
<?php
try {
    $phar = new PharData('myphar.zip');
    var_dump($phar->getMetadata());
    $phar->setMetadata("привет");
    var_dump($phar->getMetadata());
    $phar->delMetadata();
    var_dump($phar->getMetadata());
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

Результат виконання наведеного прикладу:

```
NULL
string(8) "привет"
NULL
```

### Дивіться також

-   [Phar::delMetadata()](phar.delmetadata.md) \- Видалити глобальні метадані в архіві phar
