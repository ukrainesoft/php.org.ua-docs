Застосувати зміни до документа XML

-   [« XMLDiff\\Memory::diff](xmldiff-memory.diff.html)
    
-   [XMLDiff\\File »](class.xmldiff-file.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiff\\Memory](class.xmldiff-memory.html)
    
-   Застосувати зміни до документа XML
    

# XMLDiffMemory::merge

(PECL xmldiff >= 0.8.0)

XMLDiffMemory::merge — Застосувати зміни до документа XML

### Опис

```methodsynopsis
public XMLDiff\Memory::merge(string $src, string $diff): string
```

Створює новий документ XML на базі джерела та списку змін.

### Список параметрів

`src`

XML-документ джерело.

`diff`

XML-документ, що містить інформацію про зміни.

### Значення, що повертаються

Рядок з новим XML-документом або **`null`**