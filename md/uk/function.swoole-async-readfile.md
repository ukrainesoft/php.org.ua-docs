Асинхронне читання файлу

-   [« swooleasyncread](function.swoole-async-read.html)
    
-   [swooleasyncset »](function.swoole-async-set.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Асинхронне читання файлу
    

# swooleasyncreadfile

(PECL swoole >= 1.9.0)

swooleasyncreadfile - Асинхронне читання файлу

### Опис

```methodsynopsis
swoole_async_readfile(string $filename, callable $callback): bool
```

### Список параметрів

`filename`

Ім'я файлу для читання.

`callback`

```methodsynopsis
callback(string $filename, string $content): mixed
```

`filename`

Ім'я файлу.

`content`

Вміст з файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.