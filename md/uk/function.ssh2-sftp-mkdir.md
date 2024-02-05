---
navigation:
  - function.ssh2-sftp-lstat.md: « ssh2\_sftp\_lstat
  - function.ssh2-sftp-readlink.md: ssh2\_sftp\_readlink »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp\_mkdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp\_mkdir

(PECL ssh2 >= 0.9.0)

ssh2\_sftp\_mkdir — Створити директорію

### Опис

```methodsynopsis
ssh2_sftp_mkdir(    resource $sftp,    string $dirname,    int $mode = 0777,    bool $recursive = false): bool
```

Створює директорію на сервері із заданими в `mode`правами доступа.

Функция аналогична использованию[mkdir()](function.mkdir.md) з обгорткою [ssh2.sftp://](wrappers.ssh2.md)

### Список параметрів

`sftp`

Ресурс SSH2 SFTP, відкритий за допомогою [ssh2\_sftp()](function.ssh2-sftp.md)

`dirname`

Шлях до нової директорії.

`mode`

Маска прав доступу. Фактичний режим залежить від поточного umask.

`recursive`

Якщо `recursive`задан как\*\*`true`\*\*, створюються всі батьківські директорії `dirname`якщо їх немає.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Створення директорії на віддаленому сервері**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');
$sftp = ssh2_sftp($connection);

ssh2_sftp_mkdir($sftp, '/home/username/newdir');
/* Или так:  mkdir("ssh2.sftp://$sftp/home/username/newdir"); */
?>
```

### Дивіться також

-   [mkdir()](function.mkdir.md) \- створює директорію
-   [ssh2\_sftp\_rmdir()](function.ssh2-sftp-rmdir.md) \- видаляє директорію
