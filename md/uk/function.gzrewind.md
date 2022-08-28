Перемістити вказівник gz-файлу на початок

-   [« gzread](function.gzread.html)
    
-   [gzseek »](function.gzseek.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Перемістити вказівник gz-файлу на початок
    

# gzrewind

(PHP 4, PHP 5, PHP 7, PHP 8)

gzrewind — Перемістити вказівник gz-файлу на початок

### Опис

```methodsynopsis
gzrewind(resource $stream): bool
```

Встановлює вказівник на позицію файлу початку потоку цього файла.

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [gzseek()](function.gzseek.html) - Перемістити вказівник на позицію в покажчику gz-файлу
-   [gztell()](function.gztell.html) - Повертає поточну позицію читання/запису в покажчику gz-файлу