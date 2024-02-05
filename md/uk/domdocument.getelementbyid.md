---
navigation:
  - domdocument.createtextnode.md: '« DOMDocument::createTextNode'
  - domdocument.getelementsbytagname.md: 'DOMDocument::getElementsByTagName »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::getElementById'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::getElementById

(PHP 5, PHP 7, PHP 8)

DOMDocument::getElementById — Шукає елемент із певним ідентифікатором

### Опис

```methodsynopsis
public DOMDocument::getElementById(string $elementId): ?DOMElement
```

Ця функція схожа на [DOMDocument::getElementsByTagName](domdocument.getelementsbytagname.md), але шукає елемент із заданим ідентифікатором.

Для роботи цієї функції необхідно встановити атрибути ідентифікаторів за допомогою [DOMElement::setIdAttribute](domelement.setidattribute.md)або DTD, який визначає атрибут ідентифікатора типу. В останньому випадку перед використанням цієї функції вам необхідно буде перевірити документ за допомогою [DOMDocument::validate](domdocument.validate.md) або [DOMDocument::$validateOnParse](class.domdocument.md#domdocument.props.validateonparse)

### Список параметрів

`elementId`

Унікальне значення ідентифікатора елемента.

### Значення, що повертаються

Повертає об'єкт [DOMElement](class.domelement.md)или\*\*`null`\*\*, якщо елемент не знайдено.

### Приклади

**Приклад #1 Приклад використання DOMDocument::getElementById()**

Наступні приклади використовують файл book.xml, який містить такі дані:

\]> PHP Basics Jim Smith Jane Smith [xhtml:blurb](xhtml:blurb)<!\[CDATA\[

*PHP Basics* provides an introduction to PHP.

\\\]\\\]> PHP Advanced Programming Jon Doe

```php
<?php

$doc = new DomDocument;

// Нужно проверить документ перед тем как ссылаться по идентификатору
$doc->validateOnParse = true;
$doc->Load('book.xml');

echo "Элемент с идентификатором 'php-basics': " . $doc->getElementById('php-basics')->tagName . "\n";

?>
```

Результат виконання наведеного прикладу:

```
Элемент с идентификатором 'php-basics': book
```

### Дивіться також

-   [DOMDocument::getElementsByTagName()](domdocument.getelementsbytagname.md) \- Шукає всі елементи із заданим локальним ім'ям
