Зміна прав доступу

-   [« ssh2sendeof](function.ssh2-send-eof.html)
    
-   [ssh2sftplstat »](function.ssh2-sftp-lstat.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SSH2](ref.ssh2.html)
    
-   Зміна прав доступу
    

# ssh2sftpchmod

(PECL ssh2> = 0.12)

ssh2sftpchmod — Зміна прав доступу

### Опис

```methodsynopsis
ssh2_sftp_chmod(resource $sftp, string $filename, int $mode): bool
```

Намагається змінити права доступу вказаного файлу на сервері `mode`

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.html)

`filename`

Шлях до файлу на сервері.

`mode`

Права доступу до файлу. Для більш детальної інформації дивіться опис функції [chmod()](function.chmod.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Зміна прав доступу до файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_chmod($sftp, '/somedir/somefile', 0755);
?>
```

### Дивіться також

-   [chmod()](function.chmod.html) - Змінює режим доступу до файлу
-   [ssh2sftp()](function.ssh2-sftp.html) - Ініціалізувати підсистему SFTP
-   [ssh2connect()](function.ssh2-connect.html) - Підключення до SSH-сервера