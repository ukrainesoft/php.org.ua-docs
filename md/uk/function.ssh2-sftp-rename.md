---
navigation:
  - function.ssh2-sftp-realpath.html: « ssh2sftprealpath
  - function.ssh2-sftp-rmdir.html: ssh2sftprmdir »
  - index.html: PHP Manual
  - ref.ssh2.html: Функції SSH2
title: ssh2sftprename
---
# ssh2sftprename

(PECL ssh2> = 0.9.0)

ssh2sftprename — Перейменовує файл

### Опис

```methodsynopsis
ssh2_sftp_rename(resource $sftp, string $from, string $to): bool
```

Перейменує файл на сервер.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.html)

`from`

Початковий файл.

`to`

Нове ім'я, яке замінить `from`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перейменування файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_rename($sftp, '/home/username/oldname', '/home/username/newname');
?>
```

### Дивіться також

-   [rename()](function.rename.html) - Перейменовує файл або директорію
