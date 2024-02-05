---
navigation:
  - function.ftp-append.md: « ftp\_append
  - function.ftp-chdir.md: ftp\_chdir »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_cdup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_cdup

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_cdup — Переходить до батьківської директорії

### Опис

```methodsynopsis
ftp_cdup(FTP\Connection $ftp): bool
```

Переходить у батьківську директорію.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования функции**ftp\_cdup()\*\*\*\*

```php
<?php
// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// изменение текущей директории на html
ftp_chdir($ftp, 'html');

echo ftp_pwd($ftp); // /html

// возврат в родительскую директорию
if (ftp_cdup($ftp)) {
  echo "команда cdup выполнена успешно\n";
} else {
  echo "команда cdup завершилась неудачей\n";
}

echo ftp_pwd($ftp); // /

ftp_close($ftp);
?>
```

### Дивіться також

-   [ftp\_chdir()](function.ftp-chdir.md) \- Змінює поточну директорію на FTP-сервері
-   [ftp\_pwd()](function.ftp-pwd.md) \- Повертає ім'я поточної директорії
