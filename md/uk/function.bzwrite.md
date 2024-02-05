---
navigation:
  - function.bzread.md: « bzread
  - book.lzf.md: LZF »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzwrite
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzwrite

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

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

Если указан, запись остановится после`length` (Нестиснені) записаних байт, або якщо був досягнутий кінець `data`, Залежно від того, що відбудеться першим.

### Значення, що повертаються

Повертає кількість записаних байт або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `length` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**bzwrite()\*\*\*\*

```php
<?php
$str = "uncompressed data";
$bz = bzopen("/tmp/foo.bz2", "w");
bzwrite($bz, $str, strlen($str));
bzclose($bz);
?>
```

### Дивіться також

-   [bzread()](function.bzread.md) \- Бінарно-безпечне читання файлу bzip2
-   [bzopen()](function.bzopen.md) \- Відкриває файл, стислий за допомогою bzip2
