---
navigation:
  - domdocument.createtextnode.html: '« DOMDocument::createTextNode'
  - domdocument.getelementsbytagname.html: 'DOMDocument::getElementsByTagName »'
  - index.html: PHP Manual
  - class.domdocument.html: DOMDocument
title: 'DOMDocument::getElementById'
---
# DOMDocument::getElementById

(PHP 5, PHP 7, PHP 8)

DOMDocument::getElementById — Шукає елемент із певним ідентифікатором

### Опис

```methodsynopsis
public DOMDocument::getElementById(string $elementId): ?DOMElement
```

Ця функція схожа на [DOMDocument::getElementsByTagName](domdocument.getelementsbytagname.html), але шукає елемент із заданим ідентифікатором.

Для роботи цієї функції необхідно встановити атрибути ідентифікаторів за допомогою [DOMElement::setIdAttribute](domelement.setidattribute.html)або DTD, який визначає атрибут ідентифікатора типу. В останньому випадку перед використанням цієї функції вам необхідно буде перевірити документ за допомогою [DOMDocument::validate](domdocument.validate.html) або [DOMDocument::$validateOnParse](class.domdocument.html#domdocument.props.validateonparse)

### Список параметрів

`elementId`

Унікальне значення ідентифікатора елемента.

### Значення, що повертаються

Повертає об'єкт [DOMElement](class.domelement.html) або **`null`**, якщо елемент не знайдено.

### Приклади

**Приклад #1 Приклад використання DOMDocument::getElementById()**

Наступні приклади використовують файл book.xml, який містить такі дані:

\> PHP Basics Jim Smith Jane Smith [xhtml:blurb](xhtml:blurb)

*PHP Basics* надає інформацію про PHP.

\\\]\\\]> PHP Advanced Programming Jon Doe

```php
<?php

$doc = new DomDocument;

// Нужно проверить документ перед тем как ссылаться по идентификатору
$doc->validateOnParse = true;
$doc->Load('book.xml');

echo "Элемент с идентификатором 'php-basics': " . $doc->getElementById('php-basics')->tagName . "\n";

?>
```

Результат виконання цього прикладу:

```
Элемент с идентификатором 'php-basics': book
```

### Дивіться також

-   [DOMDocument::getElementsByTagName()](domdocument.getelementsbytagname.html) - Шукає всі елементи із заданим локальним ім'ям
