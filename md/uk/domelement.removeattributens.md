Видаляє атрибут

-   [« DOMElement::removeAttributeNode](domelement.removeattributenode.html)
    
-   [DOMElement::setAttribute »](domelement.setattribute.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Видаляє атрибут
    

# DOMElement::removeAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttributeNS — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttributeNS(?string $namespace, string $localName): void
```

Видаляє атрибут `localName` у просторі імен `namespace` елемент.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.html) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttributeNS()](domelement.getattributens.html) - Повертає значення атрибуту
-   [DOMElement::setAttributeNS()](domelement.setattributens.html) - Додає новий атрибут