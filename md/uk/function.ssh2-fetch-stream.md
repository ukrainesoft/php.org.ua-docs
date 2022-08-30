Отримання розширеного потоку даних

-   [« ssh2exec](function.ssh2-exec.html)
    
-   [ssh2fingerprint »](function.ssh2-fingerprint.html)
    
-   [PHP Manual](index.md)
    
-   [Функції SSH2](ref.ssh2.md)
    
-   Отримання розширеного потоку даних
    

# ssh2fetchstream

(PECL ssh2> = 0.9.0)

ssh2fetchstream — отримання розширеного потоку даних

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
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_password($connection, 'username', 'password');

$stdio_stream = ssh2_shell($connection);
$stderr_stream = ssh2_fetch_stream($stdio_stream, SSH2_STREAM_STDERR);
?>
```

### Дивіться також

-   [ssh2shell()](function.ssh2-shell.html) - запитує інтерактивний термінал
-   [ssh2exec()](function.ssh2-exec.html) - Виконання команди на віддаленому сервері
-   [ssh2connect()](function.ssh2-connect.html) - Підключення до SSH-сервера