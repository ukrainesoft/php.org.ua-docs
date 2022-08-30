Повертає код помилки роботи з bzip2

-   [« bzdecompress](function.bzdecompress.html)
    
-   [bzerror »](function.bzerror.html)
    
-   [PHP Manual](index.html)
    
-   [Функції Bzip2](ref.bzip2.html)
    
-   Повертає код помилки роботи з bzip2
    

# bzerrno

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzerrno — Повертає код помилки роботи з bzip2

### Опис

```methodsynopsis
bzerrno(resource $bz): int
```

Повертає код будь-якої помилки bzip2, що сталася з переданим покажчиком на файл.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішний відкритий [bzopen()](function.bzopen.html)

### Значення, що повертаються

Повертає код помилки як цілого числа.

### Дивіться також

-   [bzerror()](function.bzerror.html) - Повертає код та рядок помилки роботи з bzip2 у вигляді масиву
-   [bzerrstr()](function.bzerrstr.html) - Повертає рядок помилки роботи з bzip2