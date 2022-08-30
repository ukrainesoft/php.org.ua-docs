Отримує вузол із заданим індексом

-   [« DOMNodeList::count](domnodelist.count.html)
    
-   [DOMNotation »](class.domnotation.html)
    
-   [PHP Manual](index.html)
    
-   [DOMNodeList](class.domnodelist.html)
    
-   Отримує вузол із заданим індексом
    

# DOMNodeList::item

(PHP 5, PHP 7, PHP 8)

DOMNodeList::item — Отримує вузол із заданим індексом

### Опис

```methodsynopsis
public DOMNodeList::item(int $index): DOMNode|DOMNameSpaceNode|null
```

Витягує вузол із заданим індексом `index` з об'єкту класу [DOMNodeList](class.domnodelist.html)

**Підказка**

Якщо потрібно дізнатися кількість вузлів у колекції, використовуйте властивість `length` об'єкта класу [DOMNodeList](class.domnodelist.html)

### Список параметрів

`index`

Індекс вузла в колекції.

### Значення, що повертаються

Вузол, що знаходиться в позиції `index` об'єкта [DOMNodeList](class.domnodelist.html), або \*\*`null`\*\*якщо цей індекс неприпустимий.

### Приклади

**Приклад #1 Виведення вмісту таблиці**

```php
<?php

$doc = new DOMDocument;
$doc->load('book.xml');

$items = $doc->getElementsByTagName('entry');

for ($i = 0; $i < $items->length; $i++) {
    echo $items->item($i)->nodeValue . "\n";
}

?>
```

Крім того, можна скористатися [foreach](control-structures.foreach.html);, що буде набагато зручніше:

```php
<?php

foreach ($items as $item) {
    echo $item->nodeValue . "\n";
}

?>
```

Результат виконання цього прикладу:

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