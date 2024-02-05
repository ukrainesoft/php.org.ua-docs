---
navigation:
  - phardata.delmetadata.md: '« PharData::delMetadata'
  - phardata.destruct.md: 'PharData::\_\_destruct »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::delete

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::delete — Видалити файл із tar/zip-архіву

### Опис

```methodsynopsis
public PharData::delete(string $localName): bool
```

Видаляє файл у архіві. Функціонально аналогічно виклику [unlink()](function.unlink.md) на еквіваленті потокової обгортки, як показано на прикладі нижче.

### Список параметрів

`localName`

Шлях до файлу, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, але краще використовувати перевірку винятків.

### Помилки

Викидає виняток [PharException](class.pharexception.md)в случае возникновения ошибки при сохранении изменений на диск.

### Приклади

**Приклад #1 Приклад використання** PharData::delete()\*\*\*\*

```php
<?php
try {
    $phar = new PharData('myphar.zip');
    $phar->delete('unlink/me.php');
    // аналог следующего кода:
    unlink('phar://myphar.phar/unlink/me.php');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::delete()](phar.delete.md) \- Видаляє файл усередині phar-архіву
