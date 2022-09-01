---
navigation:
  - function.ssh2-sftp-mkdir.html: « ssh2sftpmkdir
  - function.ssh2-sftp-realpath.html: ssh2sftprealpath »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2sftpreadlink
---
# ssh2sftpreadlink

(PECL ssh2> = 0.9.0)

ssh2sftpreadlink — Повертає об'єкт за символічним посиланням

### Опис

```methodsynopsis
ssh2_sftp_readlink(resource $sftp, string $link): string
```

Повертає об'єкт за символічним посиланням.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.md)

`link`

Шлях до символічного заслання.

### Значення, що повертаються

Повертає об'єкт, на який дивиться посилання `link`

### Приклади

**Приклад #1 Читання символічного посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

$target = ssh2_sftp_readlink($sftp, '/tmp/mysql.sock');
/* $target теперь такой (например): '/var/run/mysql.sock' */
?>
```

### Дивіться також

-   [readlink()](function.readlink.md) - Повертає файл, на який вказує символічне посилання
-   [ssh2sftpsymlink()](function.ssh2-sftp-symlink.md) - Створити символічне посилання
