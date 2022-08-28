Повертає поточну позицію читання/запису в покажчику gz-файлу

-   [« gzseek](function.gzseek.html)
    
-   [gzuncompress »](function.gzuncompress.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Повертає поточну позицію читання/запису в покажчику gz-файлу
    

# gztell

(PHP 4, PHP 5, PHP 7, PHP 8)

gztell — Повертає поточну позицію читання/запису в покажчику gz-файлу

### Опис

```methodsynopsis
gztell(resource $stream): int|false
```

Отримує позицію покажчика файлу, тобто зміщення потоку розпакованого файлу.

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.html)

### Значення, що повертаються

Поточна позиція або **`false`** у разі виникнення помилки.

### Дивіться також

-   [gzopen()](function.gzopen.html) - Відкрити gz-файл
-   [gzseek()](function.gzseek.html) - Перемістити вказівник на позицію в покажчику gz-файлу
-   [gzrewind()](function.gzrewind.html) - Перемістити позицію покажчик gz-файлу на початок