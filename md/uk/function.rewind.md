---
navigation:
  - function.rename.md: « rename
  - function.rmdir.md: rmdir »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: rewind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rewind

(PHP 4, PHP 5, PHP 7, PHP 8)

rewind — Скидає курсор файлового покажчика

### Опис

```methodsynopsis
rewind(resource $stream): bool
```

Встановлює курсор файлового покажчика `stream` на початок файлового потоку.

> **Зауваження** :
> 
> Якщо ви відкрили файл у режимі "запису в кінець" ("a" або "a+"), будь-які дані, які ви записуєте, будуть дописані в кінець файлу, незалежно від положення курсору.

### Список параметрів

`stream`

Файловий покажчик має бути доступним і посилатися на файл, успішно відкритий за допомогою [fopen()](function.fopen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад перезаписи**rewind()\*\*\*\*

```php
<?php
$handle = fopen('output.txt', 'r+');

fwrite($handle, 'Ужасно длинное предложение.');
rewind($handle);
fwrite($handle, 'Оп');
rewind($handle);

echo fread($handle, filesize('output.txt'));

fclose($handle);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Опасно длинное предложение.
```

### Дивіться також

-   [fread()](function.fread.md) \- Бінарно-безпечне читання файлу
-   [fseek()](function.fseek.md) \- Встановлює зміщення у файловому покажчику
-   [ftell()](function.ftell.md) \- Повертає поточну позицію покажчика читання/запису файлу
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
