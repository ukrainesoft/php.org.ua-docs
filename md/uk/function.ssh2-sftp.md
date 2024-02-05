---
navigation:
  - function.ssh2-sftp-unlink.md: « ssh2\_sftp\_unlink
  - function.ssh2-shell.md: ssh2\_shell »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_sftp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_sftp

(PECL ssh2 >= 0.9.0)

ssh2\_sftp - Ініціалізувати підсистему SFTP

### Опис

```methodsynopsis
ssh2_sftp(resource $session): resource|false
```

Запитує підсистему SFTP із вже відкритого з'єднання SSH2.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

### Значення, що повертаються

Цей метод повертає ресурс `SSH2 SFTP` для використання в інших функціях ssh2\_sftp\_\*() та обгортці [ssh2.sftp://](wrappers.ssh2.md)для fopen или\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Відкриття файлу через SFTP**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$sftp = ssh2_sftp($connection);

$stream = fopen('ssh2.sftp://' . intval($sftp) . '/path/to/file', 'r');
?>
```

### Дивіться також

-   [ssh2\_scp\_recv()](function.ssh2-scp-recv.md) \- Запит файлу через SCP
-   [ssh2\_scp\_send()](function.ssh2-scp-send.md) \- Надсилання файлу через SCP
