Закриває файл bzip2

-   [« Функции Bzip2](ref.bzip2.html)
    
-   [bzcompress »](function.bzcompress.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Bzip2](ref.bzip2.html)
    
-   Закриває файл bzip2
    

# bzclose

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzclose — Закриває файл bzip2

### Опис

```methodsynopsis
bzclose(resource $bz): bool
```

Закриває переданий покажчик файлу bzip2.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [bzopen()](function.bzopen.html) - Відкриває файл, стислий за допомогою bzip2