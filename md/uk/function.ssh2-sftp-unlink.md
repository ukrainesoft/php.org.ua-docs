---
navigation:
  - function.ssh2-sftp-symlink.html: « ssh2sftpsymlink
  - function.ssh2-sftp.html: ssh2sftp »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2sftpunlink
---
# ssh2sftpunlink

(PECL ssh2> = 0.9.0)

ssh2sftpunlink — Видалити файл на сервері

### Опис

```methodsynopsis
ssh2_sftp_unlink(resource $sftp, string $filename): bool
```

Видаляє файл на сервері.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.md)

`filename`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Видалення файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_unlink($sftp, '/home/username/stale_file');
?>
```

### Дивіться також

-   [unlink()](function.unlink.md) - Видаляє файл
