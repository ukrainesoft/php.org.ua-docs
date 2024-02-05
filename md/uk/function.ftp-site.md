---
navigation:
  - function.ftp-set-option.md: « ftp\_set\_option
  - function.ftp-size.md: ftp\_size »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_site
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_site

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_site — Надсилає серверу команду SITE

### Опис

```methodsynopsis
ftp_site(FTP\Connection $ftp, string $command): bool
```

\*\*ftp\_site()\*\*отправляет указанную команду`SITE` FTP-сервер.

Команди `SITE` не стандартизовані та залежать від FTP-сервера. Вони можуть бути корисними для зміни прав доступу до файлів або зміни власника або групи.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`command`

Команда SITE. Зверніть увагу, що цей параметр не проходить екранування спецсимволів, тому можуть виникнути проблеми з іменами, що містять пробіли та інші подібні символи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Надсилання команди SITE FTP-серверу**

```php
<?php
// Соединение с FTP-сервером
$ftp = ftp_connect('ftp.example.com');
if (!$conn) die('Не удалось подключиться к ftp.example.com');

// Вход под именем "user" с паролем "pass"
if (!ftp_login($ftp, 'user', 'pass')) die('Не удалось войти на ftp.example.com');

// Отправка "SITE CHMOD 0600 /home/user/privatefile" FTP-серверу
if (ftp_site($ftp, 'CHMOD 0600 /home/user/privatefile')) {
   echo "Команда выполнена.\n";
} else {
   die('Команда не выполнена.');
}
?>
```

### Дивіться також

-   [ftp\_raw()](function.ftp-raw.md) \- Надсилає довільну команду FTP-серверу
