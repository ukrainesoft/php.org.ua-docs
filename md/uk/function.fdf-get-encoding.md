Отримує значення ключа /Encoding

-   [« fdf\_get\_attachment](function.fdf-get-attachment.html)
    
-   [fdf\_get\_file »](function.fdf-get-file.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Отримує значення ключа /Encoding
    

# fdfgetencoding

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfgetencoding — Отримує значення ключа /Encoding

### Опис

```methodsynopsis
fdf_get_encoding(resource $fdf_document): string
```

Отримує значення ключа `/Encoding`

### Список параметрів

`fdf_document`

Дескриптор FDF-документа, повернутий функціями [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) або [fdf\_open\_string()](function.fdf-open-string.html)

### Значення, що повертаються

Повертає кодування у вигляді рядка. Повертається порожній рядок, якщо використовується схема за замовчуванням `PDFDocEncoding/Unicode`

### Дивіться також

-   [fdf\_set\_encoding()](function.fdf-set-encoding.html) - Встановлює кодування символів FDF