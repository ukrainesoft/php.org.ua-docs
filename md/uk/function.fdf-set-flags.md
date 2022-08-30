Встановлює прапор поля

-   [« fdfsetfile](function.fdf-set-file.html)
    
-   [fdfsetjavascriptaction »](function.fdf-set-javascript-action.html)
    
-   [PHP Manual](index.md)
    
-   [FDF](ref.fdf.md)
    
-   Встановлює прапор поля
    

# fdfsetflags

(PHP 4> = 4.0.2, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetflags — Встановлює прапор поля

### Опис

```methodsynopsis
fdf_set_flags(    resource $fdf_document,    string $fieldname,    int $whichFlags,    int $newFlags): bool
```

Встановлює певні прапори поля.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`whichFlags`

`newFlags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfsetopt()](function.fdf-set-opt.html) - Встановлює параметри поля