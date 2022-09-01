---
navigation:
  - function.ssh2-sftp-readlink.html: « ssh2sftpreadlink
  - function.ssh2-sftp-rename.html: ssh2sftprename »
  - index.html: PHP Manual
  - ref.ssh2.html: Функції SSH2
title: ssh2sftprealpath
---
# ssh2sftprealpath

(PECL ssh2> = 0.9.0)

ssh2sftprealpath — Визначає повний шлях по даному рядку шляхом

### Опис

```methodsynopsis
ssh2_sftp_realpath(resource $sftp, string $filename): string
```

Перетворює `filename` на повний шлях до файлу на віддаленому сервері.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2sftp()](function.ssh2-sftp.html)

`filename`

### Значення, що повертаються

Повертає повний шлях у вигляді рядка.

### Приклади

**Приклад #1 Визначення повного шляху**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

$realpath = ssh2_sftp_realpath($sftp, '/home/username/../../../..//./usr/../etc/passwd');
/* $realpath теперь: '/etc/passwd' */
?>
```

### Дивіться також

-   [realpath()](function.realpath.html) - Повертає абсолютний канонізований шлях до файлу
-   [ssh2sftpsymlink()](function.ssh2-sftp-symlink.html) - Створити символічне посилання
-   [ssh2sftpreadlink()](function.ssh2-sftp-readlink.html) - Повертає об'єкт за символічним посиланням
