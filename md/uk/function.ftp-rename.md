---
navigation:
  - function.ftp-rawlist.md: « ftp\_rawlist
  - function.ftp-rmdir.md: ftp\_rmdir »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_rename

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_rename — Перейменовує файл або директорію на FTP-сервері

### Опис

```methodsynopsis
ftp_rename(FTP\Connection $ftp, string $from, string $to): bool
```

**ftp\_rename()** перейменовує файл або директорію на сервері FTP.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`from`

Старе ім'я файлу/директорії.

`to`

Нове ім'я

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки (наприклад, при спробі перейменувати неіснуючий файл) буде викликана помилка рівня `E_WARNING`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_rename()\*\*\*\*

```php
<?php
$old_file = 'somefile.txt.bak';
$new_file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка переименовать $olf_file в $new_file
if (ftp_rename($ftp, $old_file, $new_file)) {
 echo "Файл $old_file переименован в $new_file\n";
} else {
 echo "Не удалось переименовать $old_file в $new_file\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```
