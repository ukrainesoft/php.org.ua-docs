Читає FDF документ з рядка

-   [« fdf\_next\_field\_name](function.fdf-next-field-name.html)
    
-   [fdf\_open »](function.fdf-open.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Читає FDF документ з рядка
    

# fdfopenstring

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfopenstring — Читає документ FDF з рядка

### Опис

```methodsynopsis
fdf_open_string(string $fdf_data): resource
```

Зчитує дані форми з рядка.

Ви можете використовувати **fdfopenstring()** разом із $HTTPFDFDATA для обробки введення форми FDF від віддаленого клієнта.

### Список параметрів

`fdf_data`

Дані, повернуті з PDF форми або створені за допомогою [fdf\_create()](function.fdf-create.html) і [fdf\_save\_string()](function.fdf-save-string.html)

### Значення, що повертаються

Повертає дескриптор FDF документа або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Доступ до даних форми**

```php
<?php
$fdf = fdf_open_string($HTTP_FDF_DATA);
/* ... */
fdf_close($fdf);
?>
```

### Дивіться також

-   [fdf\_open()](function.fdf-open.html) - Відкриває документ FDF
-   [fdf\_close()](function.fdf-close.html) - Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.html) - Створює новий документ FDF
-   [fdf\_save\_string()](function.fdf-save-string.html) - Повертає документ FDF у вигляді рядка