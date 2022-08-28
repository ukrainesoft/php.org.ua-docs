Отримує номер версії для FDF API або файлу

-   [« fdf\_get\_value](function.fdf-get-value.html)
    
-   [fdf\_header »](function.fdf-header.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Отримує номер версії для FDF API або файлу
    

# fdfgetversion

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfgetversion — Отримує номер версії для FDF API або файлу

### Опис

```methodsynopsis
fdf_get_version(resource $fdf_document = ?): string
```

Якщо параметр не вказано, повертає версію FDF для цього документа або номер версії API набору інструментів.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdf\_create()](function.fdf-create.html) [fdf\_open()](function.fdf-open.html) або [fdf\_open\_string()](function.fdf-open-string.html)

### Значення, що повертаються

Повертає версію у вигляді рядка. Для поточного набору інструментів FDF 5.0 номер версії API - `5.0`, а номер версії документа - `1.2` `1.3` або `1.4`

### Дивіться також

-   [fdf\_set\_version()](function.fdf-set-version.html) - Встановлює номер версії для FDF