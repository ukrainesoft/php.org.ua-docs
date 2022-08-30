Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого

-   [« XMLDiffBase::diff](xmldiff-base.diff.html)
    
-   [XMLDiffDOM »](class.xmldiff-dom.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiffBase](class.xmldiff-base.html)
    
-   Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого
    

# XMLDiffBase::merge

(PECL xmldiff >= 0.8.0)

XMLDiffBase::merge — Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого

### Опис

```methodsynopsis
abstract public XMLDiff\Base::merge(mixed $src, mixed $diff): mixed
```

Абстрактний метод порівняння для реалізації у класах спадкоємців.

Основна мета методу - створення нового документа на основі інформації про відмінності двох документів.

### Список параметрів

`src`

Початковий документ XML.

`diff`

Документ, створений методом, що реалізує абстрактний метод XMLDiffBase::diff.

### Значення, що повертаються

Залежить від реалізації.