---
navigation:
  - class.domelement.md: « DOMElement
  - domelement.append.md: 'DOMElement::append »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::after'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::after

(PHP 8)

DOMElement::after — Додає вузли після елемента

### Опис

```methodsynopsis
public DOMElement::after(DOMNode|string ...$nodes): void
```

Додає передані вузли `nodes` після елемента.

### Список параметрів

`nodes`

Вузли, які потрібно додати після вузла. Рядки автоматично перетворюються на текстові вузли.

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
| 8.3.0 | Виклик цього методу на вузлі, у якого немає батьківського вузла, тепер нічого не робить, щоб привести поведінку у відповідність до специфікації DOM. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |
| 8.3.0 | Виклик цього методу на вузлі без документа власника працює. Раніше це викидало виняток [DOMException](class.domexception.md) з кодом **`DOM_HIERARCHY_REQUEST_ERR`** |

### Приклади

**Пример #1 Пример использования метода**DOMElement::after()\*\*\*\*

Додавання вузлів після елемента Hello.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<hello/>");
$container = $doc->documentElement;

$container->after("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<hello/>
beautiful
<world/>
```

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.md) \- Додає вузли після вузла
-   [DOMElement::before()](domelement.before.md) \- Додає вузли перед елементом
