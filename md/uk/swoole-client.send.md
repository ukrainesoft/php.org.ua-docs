Надсилає дані у віддалений TCP-сокет

-   [« Swoole\\Client::resume](swoole-client.resume.html)
    
-   [Swoole\\Client::sendfile »](swoole-client.sendfile.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Client](class.swoole-client.html)
    
-   Надсилає дані у віддалений TCP-сокет
    

# SwooleClient::send

(PECL swoole >= 1.9.0)

SwooleClient::send — Надсилає дані у віддалений TCP-сокет

### Опис

```methodsynopsis
public Swoole\Client::send(string $data, string $flag = ?): int
```

### Список параметрів

`data`

Дані для відправки, які можуть бути рядковими чи двійковими

`flag`

### Значення, що повертаються

Якщо клієнт успішно надіслав дані, він повертає довжину надісланих даних. Або він повертає false та встановлює $swooleclient->errCode. Для синхронного клієнта немає обмежень на надсилання даних. Для асинхронного клієнта обмеження на надсилання даних - socketbuffersize.