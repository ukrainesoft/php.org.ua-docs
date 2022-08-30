Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff

-   [« XMLDiffDOM::diff](xmldiff-dom.diff.html)
    
-   [XMLDiffMemory »](class.xmldiff-memory.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiffDOM](class.xmldiff-dom.html)
    
-   Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff
    

# XMLDiffDOM::merge

(PECL xmldiff >= 0.8.0)

XMLDiffDOM::merge — Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff

### Опис

```methodsynopsis
public XMLDiff\DOM::merge(DOMDocument $src, DOMDocument $diff): DOMDocument
```

Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff.

### Список параметрів

`src`

Вихідний об'єкт DOMDocument.

`diff`

Об'єкт DOMDocument, що містить інформацію, отриману за допомогою XMLDiffDOM::diff.

### Значення, що повертаються

Об'єднаний DOMDocument чи NULL.