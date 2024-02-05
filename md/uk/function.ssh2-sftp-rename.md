---
navigation:
  - function.ssh2-sftp-realpath.md: « ssh2\_sftp\_realpath
  - function.ssh2-sftp-rmdir.md: ssh2\_sftp\_rmdir »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_rename

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_rename — Перейменовує файл

### Опис

```methodsynopsis
ssh2_sftp_rename(resource $sftp, string $from, string $to): bool
```

Перейменує файл на сервер.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`from`

Вихідний файл.

`to`

Новое имя, которое заменит`from`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Перейменування файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_rename($sftp, '/home/username/oldname', '/home/username/newname');
?>
```

### Дивіться також

-   [rename()](function.rename.md) \- Перейменовує файл або директорію
