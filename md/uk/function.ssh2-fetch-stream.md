---
navigation:
  - function.ssh2-exec.md: « ssh2\_exec
  - function.ssh2-fingerprint.md: ssh2\_fingerprint »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_fetch\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_fetch\_stream

(PECL ssh2 >= 0.9.0)

ssh2\_fetch\_stream — отримання розширеного потоку даних

### Опис

```methodsynopsis
ssh2_fetch_stream(resource $channel, int $streamid): resource
```

Вибирає альтернативний підтік, пов'язаний з потоком каналу SSH2. На даний момент протокол SSH2 визначає лише один підпотік STDERR, що має ідентифікатор **`SSH2_STREAM_STDERR`** (Визначений як 1).

### Список параметрів

`channel`

`streamid`

Потік каналу SSH2.

### Значення, що повертаються

Повертає запитаний ресурс потоку.

### Приклади

**Приклад #1 Відкриття консолі та отримання пов'язаного з нею потоку STDERR**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$stdio_stream = ssh2_shell($connection);
$stderr_stream = ssh2_fetch_stream($stdio_stream, SSH2_STREAM_STDERR);
?>
```

### Дивіться також

-   [ssh2\_shell()](function.ssh2-shell.md) \- запитує інтерактивний термінал
-   [ssh2\_exec()](function.ssh2-exec.md) \- Виконання команди на віддаленому сервері
-   [ssh2\_connect()](function.ssh2-connect.md) \- Підключення до SSH-сервера
