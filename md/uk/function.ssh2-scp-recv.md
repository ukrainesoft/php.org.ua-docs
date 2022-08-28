Запит файлу через SCP

-   [« ssh2\_publickey\_remove](function.ssh2-publickey-remove.html)
    
-   [ssh2\_scp\_send »](function.ssh2-scp-send.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Запит файлу через SCP
    

# ssh2scprecv

(PECL ssh2> = 0.9.0)

ssh2scprecv — Запит файлу через SCP

### Опис

```methodsynopsis
ssh2_scp_recv(resource $session, string $remote_file, string $local_file): bool
```

Копіювання файлу з сервера на клієнт за допомогою протоколу SCP.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.html)

`remote_file`

Шлях до файлу на сервері.

`local_file`

Локальний шлях для збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Завантаження файлу через SCP**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

ssh2_scp_recv($connection, '/remote/filename', '/local/filename');
?>
```

### Дивіться також

-   [ssh2\_scp\_send()](function.ssh2-scp-send.html) - Надсилання файлу через SCP
-   [copy()](function.copy.html) - Копіює файл