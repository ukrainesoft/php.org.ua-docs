---
navigation:
  - function.ssh2-sftp-readlink.md: « ssh2\_sftp\_readlink
  - function.ssh2-sftp-rename.md: ssh2\_sftp\_rename »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_realpath
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_realpath

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_realpath — Визначає повний шлях по даному рядку шляхом

### Опис

```methodsynopsis
ssh2_sftp_realpath(resource $sftp, string $filename): string
```

Перетворює ім'я файлу `filename` на повний шлях до файлу на віддаленому сервері.

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`filename`

### Значення, що повертаються

Повертає повний шлях у вигляді рядка.

### Приклади

**Приклад #1 Визначення повного шляху**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

$realpath = ssh2_sftp_realpath($sftp, '/home/username/../../../..//./usr/../etc/passwd');
/* $realpath теперь: '/etc/passwd' */
?>
```

### Дивіться також

-   [realpath()](function.realpath.md) \- Повертає абсолютний канонізований шлях до файлу
-   [ssh2\_sftp\_symlink()](function.ssh2-sftp-symlink.md) \- Створити символічне посилання
-   [ssh2\_sftp\_readlink()](function.ssh2-sftp-readlink.md) \- Повертає об'єкт за символічним посиланням
