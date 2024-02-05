---
navigation:
  - function.ssh2-sftp-stat.md: « ssh2\_sftp\_stat
  - function.ssh2-sftp-unlink.md: ssh2\_sftp\_unlink »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_symlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_symlink

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_symlink — Створити символічне посилання

### Опис

```methodsynopsis
ssh2_sftp_symlink(resource $sftp, string $target, string $link): bool
```

Створює символічне посилання з ім'ям `link`, що вказує на об'єкт `target`

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`target`

Об'єкт, який буде вказувати посилання.

`link`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Створення символічного посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_symlink($sftp, '/var/run/mysql.sock', '/tmp/mysql.sock');
?>
```

### Дивіться також

-   [ssh2\_sftp\_readlink()](function.ssh2-sftp-readlink.md) \- Повертає об'єкт за символічним посиланням
-   [symlink()](function.symlink.md) \- Створює символічне посилання
