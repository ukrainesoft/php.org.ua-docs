---
navigation:
  - function.feof.md: « feof
  - function.fgetc.md: fgetc »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: fflush
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fflush

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

fflush — Скидає буфер виводу у файл

### Опис

```methodsynopsis
fflush(resource $stream): bool
```

Ця функція здійснює скидання буферизованих даних у файл, який вказує `stream`

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.md) або [fsockopen()](function.fsockopen.md) (і все ще не закритий функцією [fclose()](function.fclose.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример записи файла с помощью**fflush()\*\*\*\*

```php
<?php
$filename = 'bar.txt';

$file = fopen($filename, 'r+');
rewind($file);
fwrite($file, 'Foo');
fflush($file);
ftruncate($file, ftell($file));
fclose($file);
?>
```

### Дивіться також

-   [clearstatcache()](function.clearstatcache.md) \- Очищає кеш стану файлів
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
