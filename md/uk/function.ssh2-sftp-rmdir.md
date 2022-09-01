---
navigation:
  - function.ssh2-sftp-rename.html: « ssh2sftprename
  - function.ssh2-sftp-stat.html: ssh2sftpstat »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2sftprmdir
---
# ssh2sftprmdir

(PECL ssh2> = 0.9.0)

ssh2sftprmdir - Видаляє директорію

### Опис

```methodsynopsis
ssh2_sftp_rmdir(resource $sftp, string $dirname): bool
```

Видаляє директорію на сервері.

Працює аналогічно [rmdir()](function.rmdir.md) з обгорткою [ssh2.sftp://](wrappers.ssh2.md)

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.md)

`dirname`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Видалення директорії на сервері**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_rmdir($sftp, '/home/username/deltodel');
/* Или так:  rmdir("ssh2.sftp://$sftp/home/username/dirtodel"); */
?>
```

### Дивіться також

-   [rmdir()](function.rmdir.md) - видаляє директорію
-   [ssh2sftpmkdir()](function.ssh2-sftp-mkdir.md) - Створити директорію
