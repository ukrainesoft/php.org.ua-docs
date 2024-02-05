---
navigation:
  - domnodelist.getiterator.md: '« DOMNodeList::getIterator'
  - class.domnotation.md: DOMNotation »
  - index.md: PHP Manual
  - class.domnodelist.md: DOMNodeList
title: 'DOMNodeList::item'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNodeList::item

(PHP 5, PHP 7, PHP 8)

DOMNodeList::item — Отримує вузол із заданим індексом

### Опис

```methodsynopsis
public DOMNodeList::item(int $index): DOMElement|DOMNode|DOMNameSpaceNode|null
```

Витягує вузол із заданим індексом `index` з об'єкту класу [DOMNodeList](class.domnodelist.md)

**Підказка**

Якщо потрібно дізнатися кількість вузлів у колекції, використовуйте властивість `length` об'єкта класу [DOMNodeList](class.domnodelist.md)

### Список параметрів

`index`

Індекс вузла в колекції.

### Значення, що повертаються

Вузол, що знаходиться в позиції `index` об'єкта [DOMNodeList](class.domnodelist.md), или\*\*`null`\*\*якщо цей індекс неприпустимий.

### Приклади

**Приклад #1 Виведення вмісту таблиці**

```php
<?php

$doc = new DOMDocument;
$doc->load('book.xml');

$items = $doc->getElementsByTagName('entry');

for ($i = 0; $i < $items->length; $i++) {
    echo $items->item($i)->nodeValue . "\n";
}

?>
```

Крім того, можна скористатися [foreach](control-structures.foreach.md);, що буде набагато зручніше:

```php
<?php

foreach ($items as $item) {
    echo $item->nodeValue . "\n";
}

?>
```

Результат виконання наведеного прикладу:

```
Title
Author
Language
ISBN
The Grapes of Wrath
John Steinbeck
en
0140186409
The Pearl
John Steinbeck
en
014017737X
Samarcande
Amine Maalouf
fr
2253051209
```
