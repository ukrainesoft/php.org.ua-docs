---
navigation:
  - function.bzopen.md: « bzopen
  - function.bzwrite.md: bzwrite »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzread
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzread

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzread - Бінарно-безпечне читання файлу bzip2

### Опис

```methodsynopsis
bzread(resource $bz, int $length = 1024): string|false
```

**bzread()** читає з переданого bzip2 файлового покажчика.

Читання зупиняється, якщо було раховано `length` (Нестиснені) байт або був досягнутий кінець файлу, залежно від того, що відбудеться раніше.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.md)

`length`

Якщо не вказано, **bzread()** зчитуватиме 1024 (нестиснутих) байтів за один раз. За один раз може бути раховано максимум 8192 байти.

### Значення, що повертаються

Повертає розпаковані дані або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**bzread()\*\*\*\*

```php
<?php

$file = "/tmp/foo.bz2";
$bz = bzopen($file, "r") or die("Невозможно открыть $file");

$decompressed_file = '';
while (!feof($bz)) {
  $decompressed_file .= bzread($bz, 4096);
}
bzclose($bz);

echo "Содержимое $file: <br />\n";
echo $decompressed_file;

?>
```

### Дивіться також

-   [bzwrite()](function.bzwrite.md) \- Бінарно-безпечний запис bzip2 файлу
-   [feof()](function.feof.md) \- Перевіряє, чи кінець файлу досягнуто
-   [bzopen()](function.bzopen.md) \- Відкриває файл, стислий за допомогою bzip2
