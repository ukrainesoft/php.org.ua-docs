Відправляє файл у віддалений TCP-сокет

-   [« SwooleClient::send](swoole-client.send.html)
    
-   [SwooleClient::sendto »](swoole-client.sendto.html)
    
-   [PHP Manual](index.md)
    
-   [SwooleClient](class.swoole-client.html)
    
-   Відправляє файл у віддалений TCP-сокет
    

# SwooleClient::sendfile

(PECL swoole >= 1.9.0)

SwooleClient::sendfile — Надсилає файл у віддалений TCP-сокет

### Опис

```methodsynopsis
public Swoole\Client::sendfile(string $filename, int $offset = ?): bool
```

Є оболонкою системного виклику sendfile в Linux.

### Список параметрів

`filename`

Шлях до файлу для надсилання.

`offset`

Зміщення файлу для надсилання

### Значення, що повертаються