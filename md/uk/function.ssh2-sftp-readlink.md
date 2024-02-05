---
navigation:
  - function.ssh2-sftp-mkdir.md: « ssh2\_sftp\_mkdir
  - function.ssh2-sftp-realpath.md: ssh2\_sftp\_realpath »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_readlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_readlink

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_readlink — Повертає об'єкт за символічним посиланням

### Опис

```methodsynopsis
ssh2_sftp_readlink(resource $sftp, string $link): string
```

Повертає об'єкт за символічним посиланням.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`link`

Шлях до символічного заслання.

### Значення, що повертаються

Повертає об'єкт, на який дивиться посилання `link`

### Приклади

**Приклад #1 Читання символічного посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

$target = ssh2_sftp_readlink($sftp, '/tmp/mysql.sock');
/* $target теперь такой (наПриклад): '/var/run/mysql.sock' */
?>
```

### Дивіться також

-   [readlink()](function.readlink.md) \- Повертає файл, на який вказує символічне посилання
-   [ssh2\_sftp\_symlink()](function.ssh2-sftp-symlink.md) \- Створити символічне посилання
