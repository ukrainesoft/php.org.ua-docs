Видаляє директорію

-   [« ssh2\_sftp\_rename](function.ssh2-sftp-rename.html)
    
-   [ssh2\_sftp\_stat »](function.ssh2-sftp-stat.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Видаляє директорію
    

# ssh2sftprmdir

(PECL ssh2> = 0.9.0)

ssh2sftprmdir - Видаляє директорію

### Опис

```methodsynopsis
ssh2_sftp_rmdir(resource $sftp, string $dirname): bool
```

Видаляє директорію на сервері.

Працює аналогічно [rmdir()](function.rmdir.html) з обгорткою [ssh2.sftp://](wrappers.ssh2.html)

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.html)

`dirname`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Видалення директорії на сервері**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_rmdir($sftp, '/home/username/deltodel');
/* Или так:  rmdir("ssh2.sftp://$sftp/home/username/dirtodel"); */
?>
```

### Дивіться також

-   [rmdir()](function.rmdir.html) - видаляє директорію
-   [ssh2\_sftp\_mkdir()](function.ssh2-sftp-mkdir.html) - Створити директорію