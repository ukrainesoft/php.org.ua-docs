Асинхронний запис даних до потоку файлу

-   [« swooleasyncset](function.swoole-async-set.html)
    
-   [swooleasyncwritefile »](function.swoole-async-writefile.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Асинхронний запис даних до потоку файлу
    

# swooleasyncwrite

(PECL swoole >= 1.9.0)

swooleasyncwrite — Асинхронний запис даних до потоку файлу

### Опис

```methodsynopsis
swoole_async_write(    string $filename,    string $content,    int $offset = ?,    callable $callback = ?): bool
```

### Список параметрів

`filename`

Ім'я файлу, в який буде зроблено запис

`content`

Вміст, що записується у файл.

`offset`

Зміщення.

`callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.