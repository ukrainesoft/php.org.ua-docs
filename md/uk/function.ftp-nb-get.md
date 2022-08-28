Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл

-   [« ftp\_nb\_fput](function.ftp-nb-fput.html)
    
-   [ftp\_nb\_put »](function.ftp-nb-put.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл
    

# ftpнбget

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

ftpнбget — Завантажує файл із FTP-сервера в асинхронному режимі та зберігає його у локальний файл

### Опис

```methodsynopsis
ftp_nb_get(    FTP\Connection $ftp,    string $local_filename,    string $remote_filename,    int $mode = FTP_BINARY,    int $offset = 0): int
```

**ftpнбget()** завантажує віддалений файл з FTP-сервера та зберігає його у локальний файл.

Різниця між цією функцією та [ftp\_get()](function.ftp-get.html) полягає в тому, що ця функція отримує файл асинхронно, так що ваша програма може здійснювати інші операції, поки файл завантажується.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`local_filename`

Шлях до локального файлу (файл буде перезаписано, якщо існує).

`remote_filename`

Шлях до віддаленого файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, або **`FTP_BINARY`**

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Тепер параметр `mode` опціональний. Раніше він був обов'язковим.                                                                                      |

### Приклади

**Приклад #1 Приклад використання **ftpнбget()****

```php
<?php

// Начало скачивания
$ret = ftp_nb_get($ftp, "test", "README", FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // Производим какие-то действия ...
   echo ".";

   // Продолжение скачивания ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При скачивании файла произошла ошибка...";
   exit(1);
}
?>
```

**Приклад #2 Відновлення завантаження файлу за допомогою **ftpнбget()****

```php
<?php

// Начало скачивания
$ret = ftp_nb_get($ftp, "test", "README", FTP_BINARY,
                      filesize("test"));
// ИЛИ: $ret = ftp_nb_get($ftp, "test", "README",
//                           FTP_BINARY, FTP_AUTORESUME);
while ($ret == FTP_MOREDATA) {

   // Производим какие-то действия ...
   echo ".";

   // Продолжение скачивания ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При скачивании файла произошла ошибка...";
   exit(1);
}
?>
```

**Приклад #3 Завантаження файлу починаючи з позиції 100 в новий файл за допомогою **ftpнбget()****

```php
<?php

// Запрет FTP_AUTOSEEK
ftp_set_option($ftp, FTP_AUTOSEEK, false);

// Начало скачивания
$ret = ftp_nb_get($ftp, "newfile", "README", FTP_BINARY, 100);
while ($ret == FTP_MOREDATA) {

   /* ... */

   // Продолжение скачивания ...
   $ret = ftp_nb_continue($ftp);
}
?>
```

В останньому прикладі, newfile буде на 100 байт менше, ніж README на FTP-сервері, тому що завантаження починається зі зміщення 100. Якщо не заборонити **`FTP_AUTOSEEK`**, перші 100 байт файлу newfile будуть містити `'\0'`

### Дивіться також

-   [ftp\_nb\_fget()](function.ftp-nb-fget.html) - Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі
-   [ftp\_nb\_continue()](function.ftp-nb-continue.html) - Продовжує асинхронну операцію
-   [ftp\_fget()](function.ftp-fget.html) - Завантажує файл з FTP-сервера та зберігає його у попередньо відкритому файлі
-   [ftp\_get()](function.ftp-get.html) - Завантажує файл із FTP-сервера