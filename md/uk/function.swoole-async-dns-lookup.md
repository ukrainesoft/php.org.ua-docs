Асинхронний та неблокуючий пошук імені хоста або IP-адреси

-   [« Функции Swoole](ref.swoole-funcs.html)
    
-   [swooleasyncread »](function.swoole-async-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Асинхронний та неблокуючий пошук імені хоста або IP-адреси
    

# swooleasyncdnslookup

(PECL swoole >= 1.9.0)

swooleasyncdnslookup — Асинхронний та неблокуючий пошук імені хоста або IP-адреси

### Опис

```methodsynopsis
swoole_async_dns_lookup(string $hostname, callable $callback): bool
```

### Список параметрів

`hostname`

Ім'я хоста.

`callback`

```methodsynopsis
callback(string $hostname, string $ip): mixed
```

`hostname`

Ім'я хоста

`IP`

IP-адреса.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.