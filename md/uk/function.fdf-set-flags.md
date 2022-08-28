Встановлює прапор поля

-   [« fdf\_set\_file](function.fdf-set-file.html)
    
-   [fdf\_set\_javascript\_action »](function.fdf-set-javascript-action.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
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

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`fieldname`

Ім'я поля FDF у вигляді рядка.

`whichFlags`

`newFlags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdf\_set\_opt()](function.fdf-set-opt.html) - Встановлює параметри поля