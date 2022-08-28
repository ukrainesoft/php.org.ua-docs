Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо

-   [« DOMXPath::\_\_construct](domxpath.construct.html)
    
-   [DOMXPath::query »](domxpath.query.html)
    
-   [PHP Manual](index.html)
    
-   [DOMXPath](class.domxpath.html)
    
-   Обчислює переданий вираз XPath і повертає типізований результат, якщо можливо
    

# DOMXPath::evaluate

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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

Додатковий параметр `registerNodeNS` можна вказати, щоб вимкнути автоматичну реєстрацію контексту вузла.

### Значення, що повертаються

Повертає типізований результат, якщо це можливо, або об'єкт [DOMNodeList](class.domnodelist.html), що містить всі вузли, що відповідають заданому XPath-виразу `expression`

Якщо `expression` побудовано неправильно або `contextNode` має неправильне значення, **DOMXPath::evaluate()** поверне **`false`**

### Приклади

**Приклад #1 Отримання всіх англійських книг**

```php
<?php

$doc = new DOMDocument;

$doc->load('book.xml');

$xpath = new DOMXPath($doc);

$tbody = $doc->getElementsByTagName('tbody')->item(0);

// запрос относительно узла tbody
$query = 'count(row/entry[. = "en"])';

$entries = $xpath->evaluate($query, $tbody);
echo "Есть $entries английские книги\n";

?>
```

Результат виконання цього прикладу:

```
Есть 2 английские книги
```

### Дивіться також

-   [DOMXPath::query()](domxpath.query.html) - Виконує заданий вираз XPath