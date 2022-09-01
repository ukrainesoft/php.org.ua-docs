---
navigation:
  - function.ssh2-forward-listen.html: « ssh2forwardlisten
  - function.ssh2-poll.html: ssh2poll »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2методівnegotiated
---
# ssh2методівnegotiated

(PECL ssh2> = 0.9.0)

ssh2методівnegotiated — Повертає список узгоджених методів

### Опис

```methodsynopsis
ssh2_methods_negotiated(resource $session): array
```

Повертає перелік узгоджених методів.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.html)

### Значення, що повертаються

### Приклади

**Приклад #1 Визначимо, які узгоджені методи**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
$methods = ssh2_methods_negotiated($connection);

echo "Ключи шифрования согласовываются методом: {$methods['kex']}\n";
echo "Сервер идентифицирован с использованием {$methods['hostkey']} и ";
echo "отпечатком: " . ssh2_fingerprint($connection) . "\n";

echo "Пакеты от клиента к серверу:\n";
echo "\tШифрование: {$methods['client_to_server']['crypt']}\n";
echo "\tСжатие: {$methods['client_to_server']['comp']}\n";
echo "\tMAC: {$methods['client_to_server']['mac']}\n";

echo "Пакеты от сервера к клиенту:\n";
echo "\tШифрование: {$methods['server_to_client']['crypt']}\n";
echo "\tСжатие: {$methods['server_to_client']['comp']}\n";
echo "\tMAC: {$methods['server_to_client']['mac']}\n";

?>
```

### Дивіться також

-   [ssh2connect()](function.ssh2-connect.html) - Підключення до SSH-сервера
