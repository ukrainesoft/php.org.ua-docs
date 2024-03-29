---
navigation:
  - domattr.construct.md: '« DOMAttr::\_\_construct'
  - class.domcdatasection.md: DOMCdataSection »
  - index.md: PHP Manual
  - class.domattr.md: DOMAttr
title: 'DOMAttr::isId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMAttr::isId

(PHP 5, PHP 7, PHP 8)

DOMAttr::isId — Перевіряє, чи є атрибут певним ідентифікатором

### Опис

```methodsynopsis
public DOMAttr::isId(): bool
```

Ця функція перевіряє, чи є певним ідентифікатором.

Відповідно до стандарту DOM для цього потрібний DTD, який визначає ідентифікатор атрибута бути ідентифікатором типу. Перед використанням цієї функції необхідно перевіряти документ на дійсність за допомогою [DOMDocument::validate](domdocument.validate.md)или`DOMDocument::validateOnParse`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання DOMAttr::isId()**

```php
<?php

$doc = new DomDocument;

// Необходимо проверить документ на действительность перед тем как ссылаться по идентификатору
$doc->validateOnParse = true;
$doc->Load('book.xml');

// Получаем атрибут элемента с именем идентификатора chapter
$attr = $doc->getElementsByTagName('chapter')->item(0)->getAttributeNode('id');

var_dump($attr->isId()); // bool(true)

?>
```
