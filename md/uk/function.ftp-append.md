---
navigation:
  - function.ftp-alloc.md: « ftp\_alloc
  - function.ftp-cdup.md: ftp\_cdup »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_append
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_append

(PHP 7 >= 7.2.0, PHP 8)

ftp\_append — Додає вміст файлу до кінця іншого файлу на FTP-сервері

### Опис

```methodsynopsis
ftp_append(    FTP\Connection $ftp,    string $remote_filename,    string $local_filename,    int $mode = FTP_BINARY): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`remote_filename`

`local_filename`

`mode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
