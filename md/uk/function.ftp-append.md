---
navigation:
  - function.ftp-alloc.html: « ftpalloc
  - function.ftp-cdup.html: ftpcdup »
  - index.html: PHP Manual
  - ref.ftp.html: Функції FTP
title: ftpappend
---
# ftpappend

(PHP 7> = 7.2.0, PHP 8)

ftpappend — Додає вміст файлу до кінця іншого файлу на FTP-сервері

### Опис

```methodsynopsis
ftp_append(    FTP\Connection $ftp,    string $remote_filename,    string $local_filename,    int $mode = FTP_BINARY): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`remote_filename`

`local_filename`

`mode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
