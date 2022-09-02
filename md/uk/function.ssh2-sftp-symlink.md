---
navigation:
  - function.ssh2-sftp-stat.md: « ssh2sftpstat
  - function.ssh2-sftp-unlink.md: ssh2sftpunlink »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2sftpsymlink
---
# ssh2sftpsymlink

(PECL ssh2> = 0.9.0)

ssh2sftpsymlink — Створити символічне посилання

### Опис

```methodsynopsis
ssh2_sftp_symlink(resource $sftp, string $target, string $link): bool
```

Створює символічне посилання з ім'ям `link`, що вказує на об'єкт `target`

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.md)

`target`

Об'єкт, який буде вказувати посилання.

`link`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створення символічного посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_symlink($sftp, '/var/run/mysql.sock', '/tmp/mysql.sock');
?>
```

### Дивіться також

-   [ssh2sftpreadlink()](function.ssh2-sftp-readlink.md) - Повертає об'єкт за символічним посиланням
-   [symlink()](function.symlink.md) - Створює символічне посилання
