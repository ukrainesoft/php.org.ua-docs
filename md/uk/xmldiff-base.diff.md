Порівняє два документи XML

-   [« XMLDiffBase::construct](xmldiff-base.construct.html)
    
-   [XMLDiffBase::merge »](xmldiff-base.merge.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiffBase](class.xmldiff-base.html)
    
-   Порівняє два документи XML
    

# XMLDiffBase::diff

(PECL xmldiff >= 0.8.0)

XMLDiffBase::diff — Порівняє два документи XML.

### Опис

```methodsynopsis
abstract public XMLDiff\Base::diff(mixed $from, mixed $to): mixed
```

Абстрактний метод порівняння для реалізації у класах спадкоємців.

Головне завдання цього - створення списку відмінностей двох документів. Порядок вхідних параметрів є важливим, оскільки від нього залежить результат.

### Список параметрів

`from`

Початковий документ XML.

`to`

XML документ, з яким проводиться порівняння.

### Значення, що повертаються

Залежить від реалізації.