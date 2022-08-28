Встановлює параметри поля

-   [« fdf\_set\_on\_import\_javascript](function.fdf-set-on-import-javascript.html)
    
-   [fdf\_set\_status »](function.fdf-set-status.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює параметри поля
    

# fdfsetopt

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetopt — Встановлює параметри поля

### Опис

```methodsynopsis
fdf_set_opt(    resource $fdf_document,    string $fieldname,    int $element,    string $str1,    string $str2): bool
```

Встановлює параметри заданого поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`element`

`str1`

`str2`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdf\_set\_flags()](function.fdf-set-flags.html) - Встановлює прапор поля