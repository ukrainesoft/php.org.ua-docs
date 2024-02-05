---
navigation:
  - domelement.after.md: '« DOMElement::after'
  - domelement.before.md: 'DOMElement::before »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::append

(PHP 8)

DOMElement::append — Додає вузли після останнього дочірнього вузла

### Опис

```methodsynopsis
public DOMElement::append(DOMNode|string ...$nodes): void
```

Додає один або кілька вузлів `nodes` до списку дочірніх вузлів після останнього дочірнього вузла.

### Список параметрів

`nodes`

Вузли, які потрібно додати. Рядки автоматично перетворюються на текстові вузли.

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
| 8.3.0 | Виклик цього методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::append()\*\*\*\*

Додавання вузлів елемент «container».

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container>hello </container>");
$world = $doc->documentElement;

$world->append("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container>hello beautiful<world/></container>
```

### Дивіться також

-   [DOMParentNode::append()](domparentnode.append.md) \- Додає вузли після останнього дочірнього вузла
-   [DOMElement::prepend()](domelement.prepend.md) \- додає вузли перед першим дочірнім вузлом
