Бінарно-безпечний запис bzip2 файлу

-   [« bzread](function.bzread.md)
    
-   [LZF »](book.lzf.md)
    
-   [PHP Manual](index.md)
    
-   [Функції Bzip2](ref.bzip2.md)
    
-   Бінарно-безпечний запис bzip2 файлу
    

# bzwrite

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzwrite - Бінарно-безпечний запис bzip2 файлу

### Опис

```methodsynopsis
bzwrite(resource $bz, string $data, ?int $length = null): int|false
```

**bzwrite()** записує рядок у переданий bzip2 файловий потік.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.md)

`data`

Дані, що записуються.

`length`

Якщо вказано, запис зупиниться після `length` (Нестиснені) записаних байт, або якщо був досягнутий кінець `data`, Залежно від того, що відбудеться першим.

### Значення, що повертаються

Повертає кількість записаних байт або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **bzwrite()****

```php
<?php
$str = "uncompressed data";
$bz = bzopen("/tmp/foo.bz2", "w");
bzwrite($bz, $str, strlen($str));
bzclose($bz);
?>
```

### Дивіться також

-   [bzread()](function.bzread.md) - Бінарно-безпечне читання файлу bzip2
-   [bzopen()](function.bzopen.md) - Відкриває файл, стислий за допомогою bzip2