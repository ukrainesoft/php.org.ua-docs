---
navigation:
  - domparentnode.prepend.md: '« DOMParentNode::prepend'
  - class.domprocessinginstruction.md: DOMProcessingInstruction »
  - index.md: PHP Manual
  - class.domparentnode.md: DOMParentNode
title: 'DOMParentNode::replaceChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMParentNode::replaceChildren

(PHP 8 >= 8.3.0)

DOMParentNode::replaceChildren — Замінює нащадків у вузлі

### Опис

```methodsynopsis
public DOMParentNode::replaceChildren(DOMNode|string ...$nodes): void
```

Замінює нащадків у вузлі.

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

**Пример #1 Пример использования метода**DOMParentNode::replaceChildren()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadHTML('<!DOCTYPE HTML><html><p>Привет!</p> проверка <p>Снова привет!</p></html>');

$dom->documentElement->replaceChildren('foo', $dom->createElement('p'), 'bar');
echo $dom->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0" standalone="yes"?>
<!DOCTYPE HTML>
<html>foo<p/>bar</html>
```
