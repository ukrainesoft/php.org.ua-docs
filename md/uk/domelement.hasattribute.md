Перевіряє, чи існує атрибут

-   [« DOMElement::getElementsByTagNameNS](domelement.getelementsbytagnamens.html)
    
-   [DOMElement::hasAttributeNS »](domelement.hasattributens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Перевіряє, чи існує атрибут
    

# DOMElement::hasAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::hasAttribute — Перевіряє, чи існує атрибут

### Опис

```methodsynopsis
public DOMElement::hasAttribute(string $qualifiedName): bool
```

Перевіряє наявність атрибута з ім'ям, вказаним у параметрі `qualifiedName` поточний елемент.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.html) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.html) - Повертає значення атрибуту
-   [DOMElement::setAttribute()](domelement.setattribute.html) - Додає новий або змінює існуючий атрибут
-   [DOMElement::removeAttribute()](domelement.removeattribute.html) - Видаляє атрибут