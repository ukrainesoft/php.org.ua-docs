---
navigation:
  - function.ftp-nb-get.md: « ftp\_nb\_get
  - function.ftp-nlist.md: ftp\_nlist »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_nb\_put
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_nb\_put

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

ftp\_nb\_put — Завантажує файл на сервер FTP в асинхронному режимі

### Опис

```methodsynopsis
ftp_nb_put(    FTP\Connection $ftp,    string $remote_filename,    string $local_filename,    int $mode = FTP_BINARY,    int $offset = 0): int|false
```

**ftp\_nb\_put()** завантажує локальний файл на сервер FTP.

Відмінність цієї функції від [ftp\_put()](function.ftp-put.md) полягає в тому, що завантаження файлу відбувається в асинхронному режимі, що дозволяє програмі виконувати інші операції під час завантаження.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`remote_filename`

Шлях до файлу на сервері.

`local_file`

Шлях до локального файлу.

`mode`

Режим передачі. Може приймати значення **`FTP_ASCII`** або **`FTP_BINARY`**

`offset`

Позиція у віддаленому файлі, в яку починається завантаження

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`** або **`false`** у разі неможливості відкрити локальний файл.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.3.0 | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Приклад #1 Приклад використання** ftp\_nb\_put()\*\*\*\*

```php
<?php

// Начало загрузки
$ret = ftp_nb_put($ftp, "test.remote", "test.local", FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // Производим какие-то действия ...
   echo ".";

   // Продолжение загрузки ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При загрузке файла произошла ошибка...";
   exit(1);
}
?>
```

**Приклад #2 Возобновление загрузки файла с помощью**ftp\_nb\_put()\*\*\*\*

```php
<?php

// Начало загрузки
$ret = ftp_nb_put($ftp, "test.remote", "test.local",
                      FTP_BINARY, ftp_size("test.remote"));
// ИЛИ: $ret = ftp_nb_put($ftp, "test.remote", "test.local",
//                           FTP_BINARY, FTP_AUTORESUME);

while ($ret == FTP_MOREDATA) {

   // Производим какие-то действия ...
   echo ".";

   // Продолжение загрузки ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При загрузке файла произошла ошибка...";
   exit(1);
}
?>
```

### Дивіться також

-   [ftp\_nb\_fput()](function.ftp-nb-fput.md) \- Завантажує заздалегідь відкритий файл на FTP-сервер в асинхронному режимі
-   [ftp\_nb\_continue()](function.ftp-nb-continue.md) \- Продовжує асинхронну операцію
-   [ftp\_put()](function.ftp-put.md) \- Завантажує файл на FTP-сервер
-   [ftp\_fput()](function.ftp-fput.md) \- Завантажує попередньо відкритий файл на FTP-сервер
