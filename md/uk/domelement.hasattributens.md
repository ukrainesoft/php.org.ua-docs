Перевіряє, чи існує заданий атрибут

-   [« DOMElement::hasAttribute](domelement.hasattribute.html)
    
-   [DOMElement::removeAttribute »](domelement.removeattribute.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Перевіряє, чи існує заданий атрибут
    

# DOMElement::hasAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::hasAttributeNS — Перевіряє, чи існує заданий атрибут

### Опис

```methodsynopsis
public DOMElement::hasAttributeNS(?string $namespace, string $localName): bool
```

Показує, чи існує атрибут у просторі імен `namespace` з ім'ям `localName` у складі елемента.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNS()](domelement.getattributens.html) - Повертає значення атрибуту
-   [DOMElement::setAttributeNS()](domelement.setattributens.html) - Додає новий атрибут
-   [DOMElement::removeAttributeNS()](domelement.removeattributens.html) - Видаляє атрибут