---
navigation:
  - function.ssh2-publickey-remove.md: « ssh2\_publickey\_remove
  - function.ssh2-scp-send.md: ssh2\_scp\_send »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_scp\_recv
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_scp\_recv

(PECL ssh2 >= 0.9.0)

ssh2\_scp\_recv — Запит файлу через SCP

### Опис

```methodsynopsis
ssh2_scp_recv(resource $session, string $remote_file, string $local_file): bool
```

Копіювання файлу з сервера на клієнт за допомогою протоколу SCP.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`remote_file`

Шлях до файлу на сервері.

`local_file`

Локальний шлях для збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Завантаження файлу через SCP**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

ssh2_scp_recv($connection, '/remote/filename', '/local/filename');
?>
```

### Дивіться також

-   [ssh2\_scp\_send()](function.ssh2-scp-send.md) \- Надсилання файлу через SCP
-   [copy()](function.copy.md) \- Копіює файл
