Видалити файл із tar/zip-архіву

-   [« PharData::delMetadata](phardata.delmetadata.html)
    
-   [PharData::destruct »](phardata.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Видалити файл із tar/zip-архіву
    

# PharData::delete

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::delete — Видалити файл із tar/zip-архіву

### Опис

```methodsynopsis
public PharData::delete(string $localName): bool
```

Видаляє файл у архіві. Функціонально аналогічно виклику [unlink()](function.unlink.html) на еквіваленті потокової обгортки, як показано на прикладі нижче.

### Список параметрів

`localName`

Шлях до файлу, що видаляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, але краще використовувати перевірку винятків.

### Помилки

Викидає виняток [PharException](class.pharexception.html) у разі виникнення помилки під час збереження змін на диск.

### Приклади

**Приклад #1 Приклад використання **PharData::delete()****

```php
<?php
try {
    $phar = new PharData('myphar.zip');
    $phar->delete('unlink/me.php');
    // аналог следующего кода:
    unlink('phar://myphar.phar/unlink/me.php');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::delete()](phar.delete.html) - Видаляє файл усередині phar-архіву