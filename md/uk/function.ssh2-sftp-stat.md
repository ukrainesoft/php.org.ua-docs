Інформація про файл

-   [« ssh2sftprmdir](function.ssh2-sftp-rmdir.html)
    
-   [ssh2sftpsymlink »](function.ssh2-sftp-symlink.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SSH2](ref.ssh2.html)
    
-   Інформація про файл
    

# ssh2sftpстати

(PECL ssh2> = 0.9.0)

ssh2sftpstat — Інформація про файл

### Опис

```methodsynopsis
ssh2_sftp_stat(resource $sftp, string $path): array
```

Інформація про файл на сервері з урахуванням символічних посилань.

Функція працює аналогічно [stat()](function.stat.html) з обгорткою [ssh2.sftp://](wrappers.ssh2.html) і повертає такі самі значення.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.html)

`path`

### Значення, що повертаються

Список значень, що повертаються дивіться в описі функції [stat()](function.stat.html)

### Приклади

**Приклад #1 Інформація про файл**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$sftp = ssh2_sftp($connection);
$statinfo = ssh2_sftp_stat($sftp, '/path/to/file');

$filesize = $statinfo['size'];
$group = $statinfo['gid'];
$owner = $statinfo['uid'];
$atime = $statinfo['atime'];
$mtime = $statinfo['mtime'];
$mode = $statinfo['mode'];
?>
```

### Дивіться також

-   [ssh2sftplstat()](function.ssh2-sftp-lstat.html) - Інформація про символічне посилання
-   [lstat()](function.lstat.html) - Повертає інформацію про файл або символічне посилання
-   [stat()](function.stat.html) - Повертає інформацію про файл