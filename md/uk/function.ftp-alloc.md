---
navigation:
  - ref.ftp.md: « Функції FTP
  - function.ftp-append.html: ftpappend »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpalloc
---
# ftpalloc

(PHP 5, PHP 7, PHP 8)

ftpalloc — Резервує місце на диску для файлу, що закачується.

### Опис

```methodsynopsis
ftp_alloc(FTP\Connection $ftp, int $size, string &$response = null): bool
```

Надсилає команду `ALLO` FTP-серверу для резервування місця під файл, що завантажується.

> **Зауваження**
> 
> Багато FTP-серверів не підтримують цю команду. Такі сервери повертають код невдачі (**`false`**), що означає відсутність підтримки цієї команди, або код успішного виконання (**`true`**), що означає, що в резервуванні немає необхідності і клієнту слід продовжувати, ніби операцію було виконано успішно. Тому цю функцію слід використовувати з серверами, які потребують обов'язкового резервування.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`size`

Кількість байт, що резервуються.

`response`

Текстове подання відповіді сервера буде повернуто за посиланням у аргумент `response`якщо він вказаний.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpalloc()****

```php
<?php

$file = "/home/user/myfile";

/* соединение с сервером */
$ftp = ftp_connect('ftp.example.com');
$login_result = ftp_login($ftp, 'anonymous', 'user@example.com');

if (ftp_alloc($ftp, filesize($file), $result)) {
  echo "Место на сервере успешно зарезервировано.  Отправляю $file.\n";
  ftp_put($conn_id, '/incoming/myfile', $file, FTP_BINARY);
} else {
  echo "Не удалось зарезервировать место на сервере. Ответ сервера: $result\n";
}

ftp_close($ftp);

?>
```

### Дивіться також

-   [ftpput()](function.ftp-put.html) - Завантажує файл на FTP-сервер
-   [ftpfput()](function.ftp-fput.html) - Завантажує попередньо відкритий файл на FTP-сервер
