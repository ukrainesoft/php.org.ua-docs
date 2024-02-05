---
navigation:
  - function.ssh2-send-eof.md: « ssh2\_send\_eof
  - function.ssh2-sftp-lstat.md: ssh2\_sftp\_lstat »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_chmod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_chmod

(PECL ssh2 >= 0.12)

ssh2\_sftp\_chmod — Зміна прав доступу

### Опис

```methodsynopsis
ssh2_sftp_chmod(resource $sftp, string $filename, int $mode): bool
```

Намагається змінити права доступу вказаного файлу на сервері `mode`

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`filename`

Шлях до файлу на сервері.

`mode`

Права доступа к файлу. Для более детальной информации смотрите описание функции[chmod()](function.chmod.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Зміна прав доступу до файлу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_chmod($sftp, '/somedir/somefile', 0755);
?>
```

### Дивіться також

-   [chmod()](function.chmod.md) \- Змінює режим доступу до файлу
-   [ssh2\_sftp()](function.ssh2-sftp.md) \- Ініціалізувати підсистему SFTP
-   [ssh2\_connect()](function.ssh2-connect.md) \- Підключення до SSH-сервера
