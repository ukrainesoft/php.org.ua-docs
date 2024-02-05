---
navigation:
  - function.ssh2-sftp-symlink.md: « ssh2\_sftp\_symlink
  - function.ssh2-sftp.md: ssh2\_sftp »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_unlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_unlink

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_unlink — Видалити файл на сервері

### Опис

```methodsynopsis
ssh2_sftp_unlink(resource $sftp, string $filename): bool
```

Видаляє файл на сервері.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`filename`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Видалення файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_unlink($sftp, '/home/username/stale_file');
?>
```

### Дивіться також

-   [unlink()](function.unlink.md) \- Видаляє файл
