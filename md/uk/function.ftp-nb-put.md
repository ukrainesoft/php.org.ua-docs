Завантажує файл на FTP-сервер в асинхронному режимі

-   [« ftpнбget](function.ftp-nb-get.html)
    
-   [ftpnlist »](function.ftp-nlist.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Завантажує файл на FTP-сервер в асинхронному режимі
    

# ftpнбput

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

ftpнбput — Завантажує файл на сервер FTP в асинхронному режимі

### Опис

```methodsynopsis
ftp_nb_put(    FTP\Connection $ftp,    string $remote_filename,    string $local_filename,    int $mode = FTP_BINARY,    int $offset = 0): int|false
```

**ftpнбput()** завантажує локальний файл на сервер FTP.

Відмінність цієї функції від [ftpput()](function.ftp-put.html) полягає в тому, що завантаження файлу відбувається в асинхронному режимі, що дозволяє програмі виконувати інші операції під час завантаження.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

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

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|        | Тепер параметр `mode` опціональний. Раніше він був обов'язковим.                                                                                  |

### Приклади

**Приклад #1 Приклад використання **ftpнбput()****

```php
<?php

// Начало загрузки
$ret = ftp_nb_put($ftp, "test.remote", "test.local", FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // Производим какие-то действия ...
   echo ".";

   // Продолжение загрузки ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При загрузке файла произошла ошибка...";
   exit(1);
}
?>
```

**Приклад #2 Відновлення завантаження файлу за допомогою **ftpнбput()****

```php
<?php

// Начало загрузки
$ret = ftp_nb_put($ftp, "test.remote", "test.local",
                      FTP_BINARY, ftp_size("test.remote"));
// ИЛИ: $ret = ftp_nb_put($ftp, "test.remote", "test.local",
//                           FTP_BINARY, FTP_AUTORESUME);

while ($ret == FTP_MOREDATA) {

   // Производим какие-то действия ...
   echo ".";

   // Продолжение загрузки ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При загрузке файла произошла ошибка...";
   exit(1);
}
?>
```

### Дивіться також

-   [ftpнбfput()](function.ftp-nb-fput.html) - Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі
-   [ftpнбcontinue()](function.ftp-nb-continue.html) - Продовжує асинхронну операцію
-   [ftpput()](function.ftp-put.html) - Завантажує файл на FTP-сервер
-   [ftpfput()](function.ftp-fput.html) - Завантажує попередньо відкритий файл на FTP-сервер