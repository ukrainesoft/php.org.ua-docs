Перейменовує файл

-   [« ssh2\_sftp\_realpath](function.ssh2-sftp-realpath.html)
    
-   [ssh2\_sftp\_rmdir »](function.ssh2-sftp-rmdir.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Перейменовує файл
    

# ssh2sftprename

(PECL ssh2> = 0.9.0)

ssh2sftprename — Перейменовує файл

### Опис

```methodsynopsis
ssh2_sftp_rename(resource $sftp, string $from, string $to): bool
```

Перейменує файл на сервер.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.html)

`from`

Початковий файл.

`to`

Нове ім'я, яке замінить `from`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перейменування файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_rename($sftp, '/home/username/oldname', '/home/username/newname');
?>
```

### Дивіться також

-   [rename()](function.rename.html) - Перейменовує файл або директорію