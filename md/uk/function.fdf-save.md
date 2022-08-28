Зберігає документ FDF

-   [« fdf\_save\_string](function.fdf-save-string.html)
    
-   [fdf\_set\_ap »](function.fdf-set-ap.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Зберігає документ FDF
    

# fdfsave

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsave — Зберігає документ FDF

### Опис

```methodsynopsis
fdf_save(resource $fdf_document, string $filename = ?): bool
```

Зберігає документ FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`filename`

Якщо зазначено, FDF буде записаний у цей параметр. В іншому випадку функція запише FDF у вихідний потік PHP за промовчанням.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdf\_close()](function.fdf-close.html) - Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.html) - Створює новий документ FDF
-   [fdf\_save\_string()](function.fdf-save-string.html) - Повертає документ FDF у вигляді рядка