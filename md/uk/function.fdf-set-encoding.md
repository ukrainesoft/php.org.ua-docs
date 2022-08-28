Встановлює кодування символів FDF

-   [« fdf\_set\_ap](function.fdf-set-ap.html)
    
-   [fdf\_set\_file »](function.fdf-set-file.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює кодування символів FDF
    

# fdfsetencoding

(PHP 4> = 4.0.7, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetencoding — Встановлює кодування символів FDF

### Опис

```methodsynopsis
fdf_set_encoding(resource $fdf_document, string $encoding): bool
```

Встановлює кодування символів для FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`encoding`

Назва кодування. Підтримуються такі значення: "`Shift-JIS`","`UHC`","`GBK`"і"`BigFive`".

Порожній рядок скидає кодування за умовчанням у схему `PDFDocEncoding/Unicode`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.