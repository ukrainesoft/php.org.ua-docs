Порівняння двох файлів XML

-   [« XMLDiff\\File](class.xmldiff-file.html)
    
-   [XMLDiff\\File::merge »](xmldiff-file.merge.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiff\\File](class.xmldiff-file.html)
    
-   Порівняння двох файлів XML
    

# XMLDiffFile::diff

(PECL xmldiff >= 0.8.0)

XMLDiffFile::diff — Порівняння двох файлів XML

### Опис

```methodsynopsis
public XMLDiff\File::diff(string $from, string $to): string
```

Порівнює два локальні файли XML і повертає рядок з інформацією про відмінності.

### Список параметрів

`from`

Шлях до джерела документа.

`to`

Шлях до цільового документа.

### Значення, що повертаються

Рядок з XML-документом, що містить інформацію про відмінності, або **`null`**