Створити символічне посилання

-   [« ssh2\_sftp\_stat](function.ssh2-sftp-stat.html)
    
-   [ssh2\_sftp\_unlink »](function.ssh2-sftp-unlink.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Створити символічне посилання
    

# ssh2sftpsymlink

(PECL ssh2> = 0.9.0)

ssh2sftpsymlink — Створити символічне посилання

### Опис

```methodsynopsis
ssh2_sftp_symlink(resource $sftp, string $target, string $link): bool
```

Створює символічне посилання з ім'ям `link`, що вказує на об'єкт `target`

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.html)

`target`

Об'єкт, який буде вказувати посилання.

`link`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створення символічного посилання**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_symlink($sftp, '/var/run/mysql.sock', '/tmp/mysql.sock');
?>
```

### Дивіться також

-   [ssh2\_sftp\_readlink()](function.ssh2-sftp-readlink.html) - Повертає об'єкт за символічним посиланням
-   [symlink()](function.symlink.html) - Створює символічне посилання