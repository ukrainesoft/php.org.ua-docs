---
navigation:
  - function.ftp-alloc.md: « ftpalloc
  - function.ftp-cdup.md: ftpcdup »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
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

Ан [FTPConnection](class.ftp-connection.md) instance.

`remote_filename`

`local_filename`

`mode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
