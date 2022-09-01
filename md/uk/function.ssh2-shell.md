---
navigation:
  - function.ssh2-sftp.html: « ssh2sftp
  - function.ssh2-tunnel.html: ssh2tunnel »
  - index.html: PHP Manual
  - ref.ssh2.html: Функції SSH2
title: ssh2shell
---
# ssh2shell

(PECL ssh2> = 0.9.0)

ssh2shell — Запитує інтерактивний термінал

### Опис

```methodsynopsis
ssh2_shell(    resource $session,    string $term_type = "vanilla",    ?array $env = null,    int $width = 80,    int $height = 25,    int $width_height_type = SSH2_TERM_UNIT_CHARS): resource|false
```

Відкриває термінал до віддаленого сервера та виділяє йому потік.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.html)

`term_type`

Тип терміналу `term_type`. Повинен відповідати одному з перелічених у серверному файлі `/etc/termcap`

`env`

`env` може містити асоціативний масив пар ім'я/значення, що представляє змінні оточення, які слід виставити в терміналі.

`width`

Ширина віртуального терміналу.

`height`

Висота віртуального терміналу.

`width_height_type`

`width_height_type` повинен бути **`SSH2_TERM_UNIT_CHARS`** або **`SSH2_TERM_UNIT_PIXELS`**

### Значення, що повертаються

Повертає ресурс ([resource](language.types.resource.html)) потоку у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Запит інтерактивного терміналу**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$stream = ssh2_shell($connection, 'vt102', null, 80, 24, SSH2_TERM_UNIT_CHARS);
?>
```

### Дивіться також

-   [ssh2exec()](function.ssh2-exec.html) - Виконання команди на віддаленому сервері
-   [ssh2tunnel()](function.ssh2-tunnel.html) - Відкрити тунель через віддалений сервер
-   [ssh2fetchstream()](function.ssh2-fetch-stream.html) - отримання розширеного потоку даних
