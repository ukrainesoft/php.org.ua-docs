---
navigation:
  - function.ssh2-shell.md: « ssh2\_shell
  - book.stomp.md: Stomp »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_tunnel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_tunnel

(PECL ssh2 >= 0.9.0)

ssh2\_tunnel — Відкрити тунель через віддалений сервер

### Опис

```methodsynopsis
ssh2_tunnel(resource $session, string $host, int $port): resource
```

Відкриває потік сокета до довільного хоста/порту за допомогою підключеного сервера SSH.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`host`

`port`

### Значення, що повертаються

### Приклади

**Приклад #1 Відкриття тунелю по довільному хосту**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_pubkey_file($connection, 'username', 'id_dsa.pub', 'id_dsa');

$tunnel = ssh2_tunnel($connection, '10.0.0.101', 12345);
?>
```

### Дивіться також

-   [ssh2\_connect()](function.ssh2-connect.md) \- Підключення до SSH-сервера
-   [fsockopen()](function.fsockopen.md) \- Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
