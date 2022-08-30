Інформація про символічне посилання

-   [« ssh2sftpchmod](function.ssh2-sftp-chmod.html)
    
-   [ssh2sftpmkdir »](function.ssh2-sftp-mkdir.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SSH2](ref.ssh2.html)
    
-   Інформація про символічне посилання
    

# ssh2sftplstat

(PECL ssh2> = 0.9.0)

ssh2sftplstat — Інформація про символічне посилання

### Опис

```methodsynopsis
ssh2_sftp_lstat(resource $sftp, string $path): array
```

Інформація про символічне посилання на серверній файловій системі *без* переходу нею.

Ця функція аналогічна використанню функції [lstat()](function.lstat.html) з обгорткою [ssh2.sftp://](wrappers.ssh2.html) і повертає такі самі значення.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.html)

`path`

Шлях до символічного заслання.

### Значення, що повертаються

Список значень, що повертаються дивіться в описі функції [stat()](function.stat.html)

### Приклади

**Приклад #1 Інформація про символічне посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$sftp = ssh2_sftp($connection);
$statinfo = ssh2_sftp_lstat($sftp, '/path/to/symlink');

$filesize = $statinfo['size'];
$group = $statinfo['gid'];
$owner = $statinfo['uid'];
$atime = $statinfo['atime'];
$mtime = $statinfo['mtime'];
$mode = $statinfo['mode'];
?>
```

### Дивіться також

-   [ssh2sftpstat()](function.ssh2-sftp-stat.html) - Інформація про файл
-   [lstat()](function.lstat.html) - Повертає інформацію про файл або символічне посилання
-   [stat()](function.stat.html) - Повертає інформацію про файл