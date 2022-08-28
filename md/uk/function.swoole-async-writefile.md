Асинхронний запис даних у файл

-   [« swoole\_async\_write](function.swoole-async-write.html)
    
-   [swoole\_clear\_error »](function.swoole-clear-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Swoole](ref.swoole-funcs.html)
    
-   Асинхронний запис даних у файл
    

# swooleasyncwritefile

(PECL swoole >= 1.9.0)

swooleasyncwritefile — Асинхронний запис даних у файл

### Опис

```methodsynopsis
swoole_async_writefile(    string $filename,    string $content,    callable $callback = ?,    int $flags = 0): bool
```

### Список параметрів

`filename`

Ім'я файлу, в який буде зроблено запис.

`content`

Вміст, що записується у файл.

`callback`

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.