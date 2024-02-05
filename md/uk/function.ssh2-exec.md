---
navigation:
  - function.ssh2-disconnect.md: « ssh2\_disconnect
  - function.ssh2-fetch-stream.md: ssh2\_fetch\_stream »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_exec

(PECL ssh2 >= 0.9.0)

ssh2\_exec — Виконання команди на віддаленому сервері

### Опис

```methodsynopsis
ssh2_exec(    resource $session,    string $command,    string $pty = ?,    array $env = ?,    int $width = 80,    int $height = 25,    int $width_height_type = SSH2_TERM_UNIT_CHARS): resource|false
```

Запуск команди на віддаленому сервері та виділення для неї каналу.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`command`

`pty`

`env`

`env` може передаватися як асоціативний масив пар ім'я/значення, які мають змінні оточення, які потрібно встановити перед запуском команди.

`width`

Ширина віртуального терміналу.

`height`

Висота віртуального терміналу.

`width_height_type`

`width_height_type` повинен бути **`SSH2_TERM_UNIT_CHARS`**или**`SSH2_TERM_UNIT_PIXELS`**

### Значення, що повертаються

Повертає потік у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Виконання команди**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$stream = ssh2_exec($connection, '/usr/local/bin/php -i');
?>
```

### Дивіться також

-   [ssh2\_connect()](function.ssh2-connect.md) \- Підключення до SSH-сервера
-   [ssh2\_shell()](function.ssh2-shell.md) \- запитує інтерактивний термінал
-   [ssh2\_tunnel()](function.ssh2-tunnel.md) \- Відкрити тунель через віддалений сервер
