Повертає документ FDF у вигляді рядка

-   [« fdf\_remove\_item](function.fdf-remove-item.html)
    
-   [fdf\_save »](function.fdf-save.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Повертає документ FDF у вигляді рядка
    

# fdfsavestring

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfsavestring — Повертає документ FDF у вигляді рядка

### Опис

```methodsynopsis
fdf_save_string(resource $fdf_document): string
```

Повертає документ FDF у вигляді рядка.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

### Значення, що повертаються

Повертає документ у вигляді рядка або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання FDF у вигляді рядка**

```php
<?php
$fdf = fdf_create();
fdf_set_value($fdf, "foo", "bar");
$str = fdf_save_string($fdf);
fdf_close($fdf);
echo $str;
?>
```

Результат виконання цього прикладу:

```
%FDF-1.2
%âãÏÓ
1 0 obj
<<
/FDF << /Fields 2 0 R >>
>>
endobj
2 0 obj
[
<< /T (foo)/V (bar)>>
]
endobj
trailer
<<
/Root 1 0 R

>>
%%EOF
```

### Дивіться також

-   [fdf\_open\_string()](function.fdf-open-string.html) - Читає FDF документ з рядка
-   [fdf\_close()](function.fdf-close.html) - Закриває FDF-документ
-   [fdf\_create()](function.fdf-create.html) - Створює новий документ FDF
-   [fdf\_save()](function.fdf-save.html) - Зберігає документ FDF