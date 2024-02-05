---
navigation:
  - function.ssh2-sftp-rename.md: « ssh2\_sftp\_rename
  - function.ssh2-sftp-stat.md: ssh2\_sftp\_stat »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_rmdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_rmdir

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_rmdir - Видаляє директорію

### Опис

```methodsynopsis
ssh2_sftp_rmdir(resource $sftp, string $dirname): bool
```

Видаляє директорію на сервері.

Працює аналогічно [rmdir()](function.rmdir.md) з обгорткою [ssh2.sftp://](wrappers.ssh2.md)

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`dirname`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Видалення директорії на сервері**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_rmdir($sftp, '/home/username/deltodel');
/* Или так:  rmdir("ssh2.sftp://$sftp/home/username/dirtodel"); */
?>
```

### Дивіться також

-   [rmdir()](function.rmdir.md) \- видаляє директорію
-   [ssh2\_sftp\_mkdir()](function.ssh2-sftp-mkdir.md) \- Створити директорію
