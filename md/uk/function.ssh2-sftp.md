---
navigation:
  - function.ssh2-sftp-unlink.html: « ssh2sftpunlink
  - function.ssh2-shell.html: ssh2shell »
  - index.html: PHP Manual
  - ref.ssh2.html: Функції SSH2
title: ssh2sftp
---
# ssh2sftp

(PECL ssh2> = 0.9.0)

ssh2sftp - Ініціалізувати підсистему SFTP

### Опис

```methodsynopsis
ssh2_sftp(resource $session): resource|false
```

Запитує підсистему SFTP із вже відкритого з'єднання SSH2.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.html)

### Значення, що повертаються

Цей метод повертає ресурс `SSH2 SFTP` для використання в інших функціях ssh2sftp() та обгортці [ssh2.sftp://](wrappers.ssh2.html) для fopen або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Відкриття файлу через SFTP**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$sftp = ssh2_sftp($connection);

$stream = fopen('ssh2.sftp://' . intval($sftp) . '/path/to/file', 'r');
?>
```

### Дивіться також

-   [ssh2scprecv()](function.ssh2-scp-recv.html) - Запит файлу через SCP
-   [ssh2scpsend()](function.ssh2-scp-send.html) - Надсилання файлу через SCP
