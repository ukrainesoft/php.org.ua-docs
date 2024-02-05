---
navigation:
  - class.domcharacterdata.md: « DOMCharacterData
  - domcharacterdata.appenddata.md: 'DOMCharacterData::appendData »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::after'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::after

(PHP 8)

DOMCharacterData::after — Додає вузли після символьних даних

### Опис

```methodsynopsis
public DOMCharacterData::after(DOMNode|string ...$nodes): void
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

**Приклад #1 Приклад использования метода**DOMCharacterData::after()\*\*\*\*

Додавання вузлів після символьних даних.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><![CDATA[hello]]></container>");
$cdata = $doc->documentElement->firstChild;

$cdata->after("beautiful", $doc->createElement("world"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container><![CDATA[hello]]>beautiful<world/></container>
```

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.md) \- Додає вузли після вузла
-   [DOMCharacterData::before()](domcharacterdata.before.md) \- Додає вузли перед вузлом
