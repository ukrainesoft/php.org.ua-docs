Повертає документ FDF у вигляді рядка

-   [« fdfremoveitem](function.fdf-remove-item.html)
    
-   [fdfsave »](function.fdf-save.html)
    
-   [PHP Manual](index.md)
    
-   [FDF](ref.fdf.md)
    
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

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

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

-   [fdfopenstring()](function.fdf-open-string.html) - Читає FDF документ з рядка
-   [fdfclose()](function.fdf-close.html) - Закриває FDF-документ
-   [fdfcreate()](function.fdf-create.html) - Створює новий документ FDF
-   [fdfsave()](function.fdf-save.html) - Зберігає документ FDF