Отримання елементів по локальному імені у заданому просторі імен

-   [« DOMElement::getElementsByTagName](domelement.getelementsbytagname.md)
    
-   [DOMElement::hasAttribute »](domelement.hasattribute.md)
    
-   [PHP Manual](index.md)
    
-   [DOMElement](class.domelement.md)
    
-   Отримання елементів по локальному імені у заданому просторі імен
    

# DOMElement::getElementsByTagNameNS

(PHP 5, PHP 7, PHP 8)

DOMElement::getElementsByTagNameNS — Отримання елементів локального імені в заданому просторі імен

### Опис

```methodsynopsis
public DOMElement::getElementsByTagNameNS(?string $namespace, string $localName): DOMNodeList
```

Ця функція вибирає всі елементи-нащадки із заданим ім'ям `localName` та простором імен `namespace`

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я. Використовуйте `*` для повернення всіх дерев'яних елементів.

### Значення, що повертаються

Ця функція повертає новий об'єкт класу [DOMNodeList](class.domnodelist.md)містить всі знайдені елементи в тому порядку, в якому вони з'являються при прямому обході дерева.

### список змін

| Версия | Описание                                  |
|--------|-------------------------------------------|
|        | `namespace` тепер допускає значення null. |

### Дивіться також

-   [DOMElement::getElementsByTagName()](domelement.getelementsbytagname.md) - Повертає елементи на ім'я тега