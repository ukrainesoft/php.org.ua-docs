Повністю видалити архів з пам'яті та з диска

-   [« Phar::stopBuffering](phar.stopbuffering.html)
    
-   [Phar::webPhar »](phar.webphar.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Повністю видалити архів з пам'яті та з диска
    

# Phar::unlinkArchive

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::unlinkArchive — Повністю видалити архів з пам'яті та з диска

### Опис

```methodsynopsis
final public static Phar::unlinkArchive(string $filename): bool
```

Повністю видаляє архів із пам'яті та з диска.

### Список параметрів

`filename`

Шлях до архіву файлової системи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі присутності відкритих файлових дескрипторів до архіву чи об'єктів [Phar](class.phar.html) [PharData](class.phardata.html) [PharFileInfo](class.pharfileinfo.html), які посилаються на цей архів, буде викинуто виняток [PharException](class.pharexception.html)

### Приклади

**Приклад #1 Приклад використання **Phar::unlinkArchive()****

```php
<?php
// простое использование
Phar::unlinkArchive('/path/to/my.phar');

// более частый вариант использования:
$p = new Phar('my.phar');
$fp = fopen('phar://my.phar/file.txt', 'r');
// создаётся 'my.phar.gz'
$gp = $p->compress(Phar::GZ);
// удаляются все ссылки на архив
unset($p);
fclose($fp);
// удаляются все следы существования
Phar::unlinkArchive('my.phar');
?>
```

### Дивіться також

-   [Phar::delete()](phar.delete.html) - Видаляє файл усередині phar-архіву
-   [Phar::offsetUnset()](phar.offsetunset.html) - Видалити файл із phar-архіву