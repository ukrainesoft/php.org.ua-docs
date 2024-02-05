---
navigation:
  - domelement.replacechildren.md: '« DOMElement::replaceChildren'
  - domelement.setattribute.md: 'DOMElement::setAttribute »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::replaceWith'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::replaceWith

(PHP 8)

DOMElement::replaceWith — Замінює елемент новими вузлами

### Опис

```methodsynopsis
public DOMElement::replaceWith(DOMNode|string ...$nodes): void
```

Замінює елемент новими вузлами `nodes`

### Список параметрів

`nodes`

Вузли для заміни. Рядки автоматично перетворюються на текстові вузли.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип одного з переданих у параметрі `nodes` елементів не допускається в типі батьківського вузла, або якщо вузол, що додається, є одним з предків цього вузла або самим цим вузлом.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо один із переданих у параметрі `nodes` елементів було створено з документа, відмінного від цього, у якому було створено цей вузол.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик методу на вузлі без батька тепер заборонено, щоб привести поведінку у відповідність до специфікації DOM. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::replaceWith()\*\*\*\*

Заміна елемента на нові вузли.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><hello/></container>");
$cdata = $doc->documentElement->firstChild;

$cdata->replaceWith("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container>beautiful<world/></container>
```

### Дивіться також

-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) \- Замінює вузол на нові вузли
-   [DOMElement::replaceChildren()](domelement.replacechildren.md) \- Замінює дочірні елементи на елементі
-   [DOMElement::after()](domelement.after.md) \- Додає вузли після елемента
-   [DOMElement::before()](domelement.before.md) \- Додає вузли перед елементом
-   [DOMElement::remove()](domelement.remove.md) \- Видаляє елемент
