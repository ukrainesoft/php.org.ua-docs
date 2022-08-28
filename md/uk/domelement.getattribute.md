Повертає значення атрибуту

-   [« DOMElement::\_\_construct](domelement.construct.html)
    
-   [DOMElement::getAttributeNode »](domelement.getattributenode.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Повертає значення атрибуту
    

# DOMElement::getAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttribute — Повертає значення атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttribute(string $qualifiedName): string
```

Повертає значення атрибуту з ім'ям `qualifiedName` для поточного сайту.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Значення атрибута або порожнє значення, якщо атрибут із зазначеним ім'ям `qualifiedName` НЕ знайдений.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::setAttribute()](domelement.setattribute.html) - Додає новий або змінює існуючий атрибут
-   [DOMElement::removeAttribute()](domelement.removeattribute.html) - Видаляє атрибут