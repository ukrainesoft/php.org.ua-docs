---
navigation:
  - function.ssh2-sftp.md: « ssh2\_sftp
  - function.ssh2-tunnel.md: ssh2\_tunnel »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_shell
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_shell

(PECL ssh2 >= 0.9.0)

ssh2\_shell — Запитує інтерактивний термінал

### Опис

```methodsynopsis
ssh2_shell(    resource $session,    string $termtype = "vanilla",    ?array $env = null,    int $width = 80,    int $height = 25,    int $width_height_type = SSH2_TERM_UNIT_CHARS): resource|false
```

Відкриває термінал до віддаленого сервера та виділяє йому потік.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.md)

`termtype`

Тип терміналу `termtype`. Повинен відповідати одному з перелічених у серверному файлі `/etc/termcap`

`env`

`env` може містити асоціативний масив пар ім'я/значення, що представляє змінні оточення, які слід виставити в терміналі.

`width`

Ширина віртуального терміналу.

`height`

Висота віртуального терміналу.

`width_height_type`

`width_height_type` повинен бути **`SSH2_TERM_UNIT_CHARS`**или**`SSH2_TERM_UNIT_PIXELS`**

### Значення, що повертаються

Повертає ресурс ([resource](language.types.resource.md)) потоку у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Запит інтерактивного терміналу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$stream = ssh2_shell($connection, 'vt102', null, 80, 24, SSH2_TERM_UNIT_CHARS);
?>
```

### Дивіться також

-   [ssh2\_exec()](function.ssh2-exec.md) \- Виконання команди на віддаленому сервері
-   [ssh2\_tunnel()](function.ssh2-tunnel.md) \- Відкрити тунель через віддалений сервер
-   [ssh2\_fetch\_stream()](function.ssh2-fetch-stream.md) \- отримання розширеного потоку даних
