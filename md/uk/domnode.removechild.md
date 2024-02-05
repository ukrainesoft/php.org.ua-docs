---
navigation:
  - domnode.normalize.md: '« DOMNode::normalize'
  - domnode.replacechild.md: 'DOMNode::replaceChild »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::removeChild'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::removeChild

(PHP 5, PHP 7, PHP 8)

DOMNode::removeChild — Видаляє дочірній вузол зі списку нащадків.

### Опис

```methodsynopsis
public DOMNode::removeChild(DOMNode $child): DOMNode|false
```

Ця функція видаляє дочірній вузол зі списку нащадків.

### Список параметрів

`child`

Дочірній вузол, що видаляється.

### Значення, що повертаються

Функція повертає дочірній вузол, що видаляється, якщо він може бути видалений або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND`**

Виникає, якщо `child`не является дочерним узлом данного узла.

### Приклади

Наступний приклад видаляє елемент `chapter`(глава) из XML-документа.

**Приклад #1 Видалення дочірнього вузла**

```php
<?php

$doc = new DOMDocument;
$doc->load('book.xml');

$book = $doc->documentElement;

// находим главу (chapter) и удалям из книги (book)
$chapter = $book->getElementsByTagName('chapter')->item(0);
$oldchapter = $book->removeChild($chapter);

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<!DOCTYPE book PUBLIC "-//OASIS//DTD DocBook XML V4.1.2//EN"
          "http://www.oasis-open.org/docbook/xml/4.1.2/docbookx.dtd">
<book id="listing">
 <title>My lists</title>

</book>
```

### Дивіться також

-   [DOMChildNode::remove()](domchildnode.remove.md) \- видаляє вузол
-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMNode::replaceChild()](domnode.replacechild.md) \- Замінює дочірній вузол
