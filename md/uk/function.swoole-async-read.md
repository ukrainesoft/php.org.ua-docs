Асинхронне читання потоку файлу

-   [« swooleasyncdnslookup](function.swoole-async-dns-lookup.html)
    
-   [swooleasyncreadfile »](function.swoole-async-readfile.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Асинхронне читання потоку файлу
    

# swooleasyncread

(PECL swoole >= 1.9.0)

swooleasyncread — Асинхронне читання потоку файлу

### Опис

```methodsynopsis
swoole_async_read(    string $filename,    callable $callback,    int $chunk_size = 65536,    int $offset = 0): bool
```

### Список параметрів

`filename`

Ім'я файлу для читання.

`callback`

```methodsynopsis
callback(string $filename, string $content): mixed
```

`filename`

Назва файлу.

`content`

Вміст, зчитаний з файлового потоку.

`chunk_size`

Довжина блоку.

`offset`

Зміщення.

### Значення, що повертаються

Чи було читання виконано успішно, чи виникла помилка.