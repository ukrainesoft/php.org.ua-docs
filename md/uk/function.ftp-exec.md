---
navigation:
  - function.ftp-delete.md: « ftp\_delete
  - function.ftp-fget.md: ftp\_fget »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_exec

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

ftp\_exec — Вимагає виконання команди на FTP-сервері

### Опис

```methodsynopsis
ftp_exec(FTP\Connection $ftp, string $command): bool
```

Надсилає команду SITE EXEC `command` на сервері FTP.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`command`

Команда для виконання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання команди (сервер надсилає код відповіді: `200`); в іншому випадку повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_exec()\*\*\*\*

```php
<?php
// инициализация переменных
$command = 'ls -al >files.txt';

// устанавливаем соединение
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// выполняем команду
if (ftp_exec($ftp, $command)) {
    echo "Команда $command выполнена успешно\n";
} else {
    echo "Не удалось выполнить $command\n";
}

// закрываем соединение
ftp_close($ftp);

?>
```

### Дивіться також

-   [ftp\_raw()](function.ftp-raw.md) \- Надсилає довільну команду FTP-серверу
