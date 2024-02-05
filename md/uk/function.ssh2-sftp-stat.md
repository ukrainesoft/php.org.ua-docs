---
navigation:
  - function.ssh2-sftp-rmdir.md: « ssh2\_sftp\_rmdir
  - function.ssh2-sftp-symlink.md: ssh2\_sftp\_symlink »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_stat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_stat

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_stat — Інформація про файл

### Опис

```methodsynopsis
ssh2_sftp_stat(resource $sftp, string $path): array
```

Інформація про файл на сервері з урахуванням символічних посилань.

Функція працює аналогічно [stat()](function.stat.md) з обгорткою [ssh2.sftp://](wrappers.ssh2.md) і повертає такі самі значення.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`path`

### Значення, що повертаються

Список значень, що повертаються дивіться в описі функції [stat()](function.stat.md)

### Приклади

**Приклад #1 Інформація про файл**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$sftp = ssh2_sftp($connection);
$statinfo = ssh2_sftp_stat($sftp, '/path/to/file');

$filesize = $statinfo['size'];
$group = $statinfo['gid'];
$owner = $statinfo['uid'];
$atime = $statinfo['atime'];
$mtime = $statinfo['mtime'];
$mode = $statinfo['mode'];
?>
```

### Дивіться також

-   [ssh2\_sftp\_lstat()](function.ssh2-sftp-lstat.md) \- Інформація про символічне посилання
-   [lstat()](function.lstat.md) \- Повертає інформацію про файл або символічне посилання
-   [stat()](function.stat.md) \- Повертає інформацію про файл
