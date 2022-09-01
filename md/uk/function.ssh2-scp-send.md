---
navigation:
  - function.ssh2-scp-recv.html: « ssh2scprecv
  - function.ssh2-send-eof.html: ssh2sendeof »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2scpsend
---
# ssh2scpsend

(PECL ssh2> = 0.9.0)

ssh2scpsend — Надсилання файлу через SCP

### Опис

```methodsynopsis
ssh2_scp_send(    resource $session,    string $local_file,    string $remote_file,    int $create_mode = 0644): bool
```

Копіювання файлу з клієнта на сервер за допомогою протоколу SCP.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2connect()](function.ssh2-connect.md)

`local_file`

Шлях до локального файлу.

`remote_file`

Шлях на сервері, куди буде збережено файл.

`create_mode`

Файл буде створено з правами доступу, зазначеними в `create_mode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Завантаження файлу на сервер через SCP**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

ssh2_scp_send($connection, '/local/filename', '/remote/filename', 0644);
?>
```

### Дивіться також

-   [ssh2scprecv()](function.ssh2-scp-recv.md) - Запит файлу через SCP
-   [copy()](function.copy.md) - Копіює файл
