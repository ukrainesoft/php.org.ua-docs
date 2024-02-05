---
navigation:
  - domcharacterdata.appenddata.md: '« DOMCharacterData::appendData'
  - domcharacterdata.deletedata.md: 'DOMCharacterData::deleteData »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::before'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::before

(PHP 8)

DOMCharacterData::before — Додає вузли перед вузлом.

### Опис

```methodsynopsis
public DOMCharacterData::before(DOMNode|string ...$nodes): void
```

Додає передані вузли `nodes`перед узлом.

### Список параметрів

`nodes`

Вузли, які потрібно додати перед вузлом. Рядки автоматично перетворюються на текстові вузли.

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

### Приклади

**Приклад #1 Приклад использования метода**DOMCharacterData::before()\*\*\*\*

Додавання вузлів перед символьними даними.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><![CDATA[world]]></container>");
$cdata = $doc->documentElement->firstChild;

$cdata->before("hello", $doc->createElement("beautiful"));

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container>hello<beautiful/><![CDATA[world]]></container>
```

### Дивіться також

-   [DOMChildNode::before()](domchildnode.before.md) \- Додає вузли перед вузлом
-   [DOMCharacterData::after()](domcharacterdata.after.md) \- Додає вузли після символьних даних
