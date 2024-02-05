---
navigation:
  - domxpath.construct.md: '« DOMXPath::\_\_construct'
  - domxpath.query.md: 'DOMXPath::query »'
  - index.md: PHP Manual
  - class.domxpath.md: DOMXPath
title: 'DOMXPath::evaluate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMXPath::evaluate

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

DOMXPath::evaluate — Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо

### Опис

```methodsynopsis
public DOMXPath::evaluate(string $expression, ?DOMNode $contextNode = null, bool $registerNodeNS = true): mixed
```

Виконує переданий вираз XPath `expression` та повертає типізований результат, якщо це можливо.

### Список параметрів

`expression`

Вираз XPath для виконання.

`contextNode`

Додатковий параметр `contextNode` може бути вказаний до виконання відносних запитів XPath. За промовчанням запити виконуються щодо кореневого елемента.

`registerNodeNS`

Чи потрібно автоматично реєструвати префікси простору імен в області видимості контекстного вузла для об'єкта [DOMXPath](class.domxpath.md). Параметр допомагає уникати ручного виклику методу [DOMXPath::registerNamespace()](domxpath.registernamespace.md) для кожного простору імен у області видимості. Коли префікси простору імен конфліктують, реєструється лише префікс простору імен найближчого нащадка.

### Значення, що повертаються

Повертає типізований результат, якщо це можливо, або об'єкт [DOMNodeList](class.domnodelist.md), що містить всі вузли, що відповідають заданому XPath-виразу `expression`

Якщо `expression`построено неправильно или`contextNode`имеет неверное значение,**DOMXPath::evaluate()** поверне **`false`**

### Приклади

**Приклад #1 Отримання всіх англійських книг**

```php
<?php

$doc = new DOMDocument;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

$tbody = $doc->getElementsByTagName('tbody')->item(0);

// запрос относительно узла tbody
$query = 'count(row/entry[. = "en"])';

$entries = $xpath->evaluate($query, $tbody);
echo "Есть $entries английские книги\n";

?>
```

Результат виконання наведеного прикладу:

```
Есть 2 английские книги
```

### Дивіться також

-   [DOMXPath::query()](domxpath.query.md) \- Виконує заданий вираз XPath
