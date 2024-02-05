---
navigation:
  - function.ftell.md: « ftell
  - function.fwrite.md: fwrite »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: ftruncate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftruncate

(PHP 4, PHP 5, PHP 7, PHP 8)

ftruncate — Урізує файл до вказаної довжини

### Опис

```methodsynopsis
ftruncate(resource $stream, int $size): bool
```

Приймає файловий покажчик `stream`и урезает соответствующий файл до размера`size`

### Список параметрів

`stream`

Файловий покажчик.

> **Зауваження** :
> 
> `stream` має бути відкрито для запису.

`size`

Розмір файлу, до якого він буде обрізаний.

> **Зауваження** :
> 
> Якщо `size` більше поточного розміру файлу, файл буде доповнений нульовими байтами.
> 
> Якщо `size` менше поточного розміру файлу, файл буде обрізаний до цього розміру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад обрізання файлу**

```php
<?php
$filename = 'lorem_ipsum.txt';

$handle = fopen($filename, 'r+');
ftruncate($handle, rand(1, filesize($filename)));
rewind($handle);
echo fread($handle, filesize($filename));
fclose($handle);
?>
```

### Примітки

> **Зауваження** :
> 
> Файловий покажчик *не*меняется.

### Дивіться також

-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [fseek()](function.fseek.md) \- Встановлює зміщення у файловому покажчику
