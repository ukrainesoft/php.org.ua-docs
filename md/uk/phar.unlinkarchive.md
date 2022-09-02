---
navigation:
  - phar.stopbuffering.md: '« Phar::stopBuffering'
  - phar.webphar.md: 'Phar::webPhar »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::unlinkArchive'
---
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

У разі присутності відкритих файлових дескрипторів до архіву чи об'єктів [Phar](class.phar.md) [PharData](class.phardata.md) [PharFileInfo](class.pharfileinfo.md), які посилаються на цей архів, буде викинуто виняток [PharException](class.pharexception.md)

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

-   [Phar::delete()](phar.delete.md) - Видаляє файл усередині phar-архіву
-   [Phar::offsetUnset()](phar.offsetunset.md) - Видалити файл із phar-архіву
