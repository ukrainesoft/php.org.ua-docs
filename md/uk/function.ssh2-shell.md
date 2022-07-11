- [« ssh2_sftp](function.ssh2-sftp.md)
- [ssh2_tunnel »](function.ssh2-tunnel.md)

- [PHP Manual](index.md)
- [Функції SSH2](ref.ssh2.md)
- запитує інтерактивний термінал

# ssh2_shell

(PECL ssh2 \>= 0.9.0)

ssh2_shell — Запитує інтерактивний термінал

### Опис

**ssh2_shell**(
resource `$session`,
string `$term_type` = "vanilla",
?array `$env` = **`null`**,
int `$width` = 80,
int `$height` = 25,
int `$width_height_type` = SSH2_TERM_UNIT_CHARS
): resource \ | false

Відкриває термінал до віддаленого сервера та виділяє йому потік.

### Список параметрів

`session`
Ідентифікатор з'єднання SSH, отриманий з
[ssh2_connect()](function.ssh2-connect.md).

`term_type`
Тип терміналу `term_type`. Повинен відповідати одному з
перерахованих у серверному файлі `/etc/termcap`.

`env`
`env` може містити асоціативний масив пар ім'я/значення,
що представляє змінні оточення, які треба виставити у терміналі.

`width`
Ширина віртуального терміналу.

`height`
Висота віртуального терміналу.

`width_height_type`
`width_height_type` має бути **`SSH2_TERM_UNIT_CHARS`** або
**`SSH2_TERM_UNIT_PIXELS`**.

### Значення, що повертаються

Повертає ресурс ([resource](language.types.resource.md)) потоку в
у разі успішного виконання або **`false`** у разі виникнення
помилки.

### Приклади

**Приклад #1 Запит інтерактивного терміналу**

` <?php$connection = ssh2_connect('shell.example.com', 22);ssh2_auth_password($connection, 'username', 'password');$stream = ssh2_shell($connection, 'vt102', null, null, 24, SSH2_TERM_UNIT_CHARS);?> `

### Дивіться також

- [ssh2_exec()](function.ssh2-exec.md) - Виконання команди на
віддаленому сервері
- [ssh2_tunnel()](function.ssh2-tunnel.md) - Відкрити тунель через
віддалений сервер
- [ssh2_fetch_stream()](function.ssh2-fetch-stream.md) - Отримання
розширеного потоку даних
