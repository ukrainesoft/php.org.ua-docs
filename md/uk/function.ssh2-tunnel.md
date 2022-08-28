Відкрити тунель через віддалений сервер

-   [« ssh2\_shell](function.ssh2-shell.html)
    
-   [Stomp »](book.stomp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SSH2](ref.ssh2.html)
    
-   Відкрити тунель через віддалений сервер
    

# ssh2tunnel

(PECL ssh2> = 0.9.0)

ssh2tunnel — Відкрити тунель через віддалений сервер

### Опис

```methodsynopsis
ssh2_tunnel(resource $session, string $host, int $port): resource
```

Відкриває потік сокета до довільного хоста/порту за допомогою підключеного сервера SSH.

### Список параметрів

`session`

Ідентифікатор з'єднання SSH, отриманий з [ssh2\_connect()](function.ssh2-connect.html)

`host`

`port`

### Значення, що повертаються

### Приклади

**Приклад #1 Відкриття тунелю по довільному хосту**

```php
<?php
$connection = ssh2_connect('shell.example.com', 22);
ssh2_auth_pubkey_file($connection, 'username', 'id_dsa.pub', 'id_dsa');

$tunnel = ssh2_tunnel($connection, '10.0.0.101', 12345);
?>
```

### Дивіться також

-   [ssh2\_connect()](function.ssh2-connect.html) - Підключення до SSH-сервера
-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix