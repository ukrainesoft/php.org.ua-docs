---
navigation:
  - domelement.removeattributens.md: '« DOMElement::removeAttributeNS'
  - domelement.replacewith.md: 'DOMElement::replaceWith »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::replaceChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::replaceChildren

(PHP 8 >= 8.3.0)

DOMElement::replaceChildren — Замінює дочірні елементи в елементі

### Опис

```methodsynopsis
public DOMElement::replaceChildren(DOMNode|string ...$nodes): void
```

Замінює дочірні елементи елемента новими вузлами `nodes`

### Список параметрів

`nodes`

Вузли, якими будуть замінені нащадки. Рядки автоматично перетворюються на текстові вузли.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_HIERARCHY_REQUEST_ERR`**

Виникає, якщо тип одного з переданих у параметрі `nodes` елементів не допускається в типі вузла, або якщо вузол, що додається, є одним з предків цього вузла або самим цим вузлом.

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо один із переданих у параметрі `nodes` елементів було створено з документа, відмінного від цього, у якому було створено цей вузол.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::replaceChildren()\*\*\*\*

Заміна дочірніх вузлів на нові.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><hello/></container>");
$container = $doc->documentElement;

$container->replaceWith("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
beautiful
<world/>
```

### Дивіться також

-   [DOMParentNode::replaceChildren()](domparentnode.replacechildren.md) \- Замінює нащадків у вузлі
-   [DOMElement::replaceWith()](domelement.replacewith.md) \- Замінює елемент новими вузлами
-   [DOMElement::after()](domelement.after.md) \- Додає вузли після елемента
-   [DOMElement::before()](domelement.before.md) \- Додає вузли перед елементом
-   [DOMElement::remove()](domelement.remove.md) \- Видаляє елемент
