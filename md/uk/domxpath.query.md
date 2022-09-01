---
navigation:
  - domxpath.evaluate.md: '« DOMXPath::evaluate'
  - domxpath.registernamespace.md: 'DOMXPath::registerNamespace »'
  - index.md: PHP Manual
  - class.domxpath.md: DOMXPath
title: 'DOMXPath::query'
---
# DOMXPath::query

(PHP 5, PHP 7, PHP 8)

DOMXPath::query — Виконує заданий вираз XPath

### Опис

```methodsynopsis
public DOMXPath::query(string $expression, ?DOMNode $contextNode = null, bool $registerNodeNS = true): mixed
```

Виконує заданий XPath-вираз `expression`

### Список параметрів

`expression`

Вираз XPath для виконання.

`contextNode`

Додатковий параметр `contextNode` може бути вказаний до виконання відносних запитів XPath. За промовчанням запити виконуються щодо кореневого елемента.

`registerNodeNS`

Додатковий параметр `registerNodeNS` можна вказати, щоб вимкнути автоматичну реєстрацію контексту вузла.

### Значення, що повертаються

Повертає об'єкт [DOMNodeList](class.domnodelist.md), що містить вузли, що відповідають виразу XPath `expression`. Будь-який вираз, що не повертає вузли, поверне порожній об'єкт [DOMNodeList](class.domnodelist.md)

Якщо `expression` побудовано неправильно або `contextNode` має неправильне значення, **DOMXPath::query()** поверне **`false`**

### Приклади

**Приклад #1 Отримання списку всіх книг англійською**

```php
<?php

$doc = new DOMDocument;

// Не хотим возиться с пробелами
$doc->preserveWhiteSpace = false;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

// Начинаем с корневого элемента
$query = '//book/chapter/para/informaltable/tgroup/tbody/row/entry[. = "en"]';

$entries = $xpath->query($query);

foreach ($entries as $entry) {
    echo "Найдена книга {$entry->previousSibling->previousSibling->nodeValue}," .
         " автор {$entry->previousSibling->nodeValue}\n";
}
?>
```

Результат виконання цього прикладу:

```
Найдена книга The Grapes of Wrath, автор John Steinbeck
Найдена книга The Pearl, автор John Steinbeck
```

Можна також використовувати параметр `contextNode` для більш короткого запису виразу:

```php
<?php

$doc = new DOMDocument;
$doc->preserveWhiteSpace = false;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

$tbody = $doc->getElementsByTagName('tbody')->item(0);

// запрос относительно узла tbody
$query = 'row/entry[. = "en"]';

$entries = $xpath->query($query, $tbody);

foreach ($entries as $entry) {
    echo "Найдена книга {$entry->previousSibling->previousSibling->nodeValue}," .
         " автор {$entry->previousSibling->nodeValue}\n";
}
?>
```

### Дивіться також

-   [DOMXPath::evaluate()](domxpath.evaluate.md) - Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо
