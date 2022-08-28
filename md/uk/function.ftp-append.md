Додає вміст файлу до кінця іншого файлу на FTP-сервері

-   [« ftp\_alloc](function.ftp-alloc.html)
    
-   [ftp\_cdup »](function.ftp-cdup.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Додає вміст файлу до кінця іншого файлу на FTP-сервері
    

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

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`remote_filename`

`local_filename`

`mode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |