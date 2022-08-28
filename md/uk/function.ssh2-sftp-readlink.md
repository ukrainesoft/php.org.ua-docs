Повертає об'єкт за символічним посиланням

-   [« ssh2\_sftp\_mkdir](function.ssh2-sftp-mkdir.html)
    
-   [ssh2\_sftp\_realpath »](function.ssh2-sftp-realpath.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Повертає об'єкт за символічним посиланням
    

# ssh2sftpreadlink

(PECL ssh2> = 0.9.0)

ssh2sftpreadlink — Повертає об'єкт за символічним посиланням

### Опис

```methodsynopsis
ssh2_sftp_readlink(resource $sftp, string $link): string
```

Повертає об'єкт за символічним посиланням.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.html)

`link`

Шлях до символічного заслання.

### Значення, що повертаються

Повертає об'єкт, на який дивиться посилання `link`

### Приклади

**Приклад #1 Читання символічного посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

$target = ssh2_sftp_readlink($sftp, '/tmp/mysql.sock');
/* $target теперь такой (например): '/var/run/mysql.sock' */
?>
```

### Дивіться також

-   [readlink()](function.readlink.html) - Повертає файл, на який вказує символічне посилання
-   [ssh2\_sftp\_symlink()](function.ssh2-sftp-symlink.html) - Створити символічне посилання