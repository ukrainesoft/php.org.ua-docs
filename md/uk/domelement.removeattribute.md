Видаляє атрибут

-   [« DOMElement::hasAttributeNS](domelement.hasattributens.html)
    
-   [DOMElement::removeAttributeNode »](domelement.removeattributenode.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Видаляє атрибут
    

# DOMElement::removeAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttribute — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttribute(string $qualifiedName): bool
```

Видаляє атрибут з ім'ям `qualifiedName` елемент.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо атрибут доступний лише для читання.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.html) - Повертає значення атрибуту
-   [DOMElement::setAttribute()](domelement.setattribute.html) - Додає новий або змінює існуючий атрибут