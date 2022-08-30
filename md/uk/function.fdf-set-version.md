Встановлює номер версії для FDF

-   [« fdfsetvalue](function.fdf-set-value.html)
    
-   [GnuPG »](book.gnupg.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Встановлює номер версії для FDF
    

# fdfsetversion

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdfsetversion — Встановлює номер версії для файлу FDF

### Опис

```methodsynopsis
fdf_set_version(resource $fdf_document, string $version): bool
```

Встановлює `version` FDF для цього документа.

Деякі функції, які підтримує модуль, доступні лише в нових версіях FDF.

### Список параметрів

`fdf_document`

Дескриптор документа FDF, що повертається [fdfcreate()](function.fdf-create.html) [fdfopen()](function.fdf-open.html) ор [fdfopenstring()](function.fdf-open-string.html)

`version`

Номер версії. Для поточного набору інструментів FDF 5.0 це може бути `1.2` `1.3` або `1.4`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fdfgetversion()](function.fdf-get-version.html) - Отримує номер версії для FDF API або файлу