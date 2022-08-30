Створює спеціальний fifo файл (іменований канал-pipe)

-   [« posixkill](function.posix-kill.html)
    
-   [posixmknod »](function.posix-mknod.html)
    
-   [PHP Manual](index.html)
    
-   [POSIX Функции](ref.posix.html)
    
-   Створює спеціальний fifo файл (іменований канал-pipe)
    

# posixmkfifo

(PHP 4, PHP 5, PHP 7, PHP 8)

posixmkfifo - Створює спеціальний fifo файл (іменований канал-pipe)

### Опис

```methodsynopsis
posix_mkfifo(string $filename, int $permissions): bool
```

**posixmkfifo()** створює спеціальний `FIFO` файл, який існує у файловій системі і виступає як двоспрямований зв'язок для процесів.

### Список параметрів

`filename`

Шлях до `FIFO` файлу.

`permissions`

Другий параметр `permissions` має бути представлений у восьмеричній нотації (наприклад 0644). Це рівень прав для новоствореного `FIFO` файлу, також залежить від налаштувань поточного [umask()](function.umask.html). Права на створений файл будуть визначатися як результат (mode & umask).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.