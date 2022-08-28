Встановлює зовнішній вигляд поля

-   [« fdf\_save](function.fdf-save.html)
    
-   [fdf\_set\_encoding »](function.fdf-set-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює зовнішній вигляд поля
    

# fdfsetап

(PHP 4, PHP 5 < 5.3.0, PECL fdf SVN)

fdfsetap — Встановлює зовнішній вигляд поля

### Опис

```methodsynopsis
fdf_set_ap(    resource $fdf_document,    string $field_name,    int $face,    string $filename,    int $page_number): bool
```

Встановлює зовнішній вигляд поля (тобто значення ключа `/AP`

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) ор [fdf\_open\_string()](function.fdf-open-string.html)

`field_name`

`face`

Допустимі значення: **`FDFNormalAP`** **`FDFRolloverAP`** і **`FDFDownAP`**

`filename`

`page_number`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.