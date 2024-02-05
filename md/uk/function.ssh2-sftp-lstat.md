---
navigation:
  - function.ssh2-sftp-chmod.md: « ssh2\_sftp\_chmod
  - function.ssh2-sftp-mkdir.md: ssh2\_sftp\_mkdir »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_lstat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_lstat

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_lstat — Інформація про символічне посилання

### Опис

```methodsynopsis
ssh2_sftp_lstat(resource $sftp, string $path): array
```

Інформація про символічне посилання на серверній файловій системі *без* перехода по ней.

Ця функція аналогічна використанню функції [lstat()](function.lstat.md) з обгорткою [ssh2.sftp://](wrappers.ssh2.md) і повертає такі самі значення.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`path`

Шлях до символічного заслання.

### Значення, що повертаються

Список значень, що повертаються дивіться в описі функції [stat()](function.stat.md)

### Приклади

**Приклад #1 Інформація про символічне посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$sftp = ssh2_sftp($connection);
$statinfo = ssh2_sftp_lstat($sftp, '/path/to/symlink');

$filesize = $statinfo['size'];
$group = $statinfo['gid'];
$owner = $statinfo['uid'];
$atime = $statinfo['atime'];
$mtime = $statinfo['mtime'];
$mode = $statinfo['mode'];
?>
```

### Дивіться також

-   [ssh2\_sftp\_stat()](function.ssh2-sftp-stat.md) \- Інформація про файл
-   [lstat()](function.lstat.md) \- Повертає інформацію про файл або символічне посилання
-   [stat()](function.stat.md) \- Повертає інформацію про файл
