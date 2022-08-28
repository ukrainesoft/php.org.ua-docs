Повертає рядок помилки роботи з bzip2

-   [« bzerror](function.bzerror.html)
    
-   [bzflush »](function.bzflush.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Bzip2](ref.bzip2.html)
    
-   Повертає рядок помилки роботи з bzip2
    

# bzerrstr

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

bzerrstr — Повертає рядок помилки роботи з bzip2

### Опис

```methodsynopsis
bzerrstr(resource $bz): string
```

Повертає рядок з помилкою bzip2, що сталася з переданим покажчиком файлу.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.html)

### Значення, що повертаються

Повертає рядок, який містить повідомлення про помилку.

### Дивіться також

-   [bzerrno()](function.bzerrno.html) - Повертає код помилки роботи з bzip2
-   [bzerror()](function.bzerror.html) - Повертає код та рядок помилки роботи з bzip2 у вигляді масиву