Повертає елементи на ім'я тега

-   [« DOMElement::getAttributeNS](domelement.getattributens.html)
    
-   [DOMElement::getElementsByTagNameNS »](domelement.getelementsbytagnamens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Повертає елементи на ім'я тега
    

# DOMElement::getElementsByTagName

(PHP 5, PHP 7, PHP 8)

DOMElement::getElementsByTagName — Повертає елементи на ім'я тега

### Опис

```methodsynopsis
public DOMElement::getElementsByTagName(string $qualifiedName): DOMNodeList
```

Ця функція повертає новий екземпляр класу [DOMNodeList](class.domnodelist.html) - список всіх елементів-нащадків поточного вузла із вказаним ім'ям тега `qualifiedName`в тому порядку, в якому вони зустрічаються при обході дерева.

### Список параметрів

`qualifiedName`

Ім'я тег. Використовуйте символ `*` для всіх елементів дерева.

### Значення, що повертаються

Ця функція повертає новий об'єкт класу [DOMNodeList](class.domnodelist.html) - Список всіх відповідних елементів.

### Дивіться також

-   [DOMElement::getElementsByTagNameNS()](domelement.getelementsbytagnamens.html) - Отримання елементів по локальному імені у заданому просторі імен