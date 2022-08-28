Перевіряє, чи є атрибут певним ідентифікатором

-   [« DOMAttr::\_\_construct](domattr.construct.html)
    
-   [DOMCdataSection »](class.domcdatasection.html)
    
-   [PHP Manual](index.html)
    
-   [DOMAttr](class.domattr.html)
    
-   Перевіряє, чи є атрибут певним ідентифікатором
    

# DOMAttr::isId

(PHP 5, PHP 7, PHP 8)

DOMAttr::isId — Перевіряє, чи є атрибут певним ідентифікатором

### Опис

```methodsynopsis
public DOMAttr::isId(): bool
```

Ця функція перевіряє, чи є певним ідентифікатором.

Відповідно до стандарту DOM для цього потрібний DTD, який визначає ідентифікатор атрибута бути ідентифікатором типу. Перед використанням цієї функції необхідно перевіряти документ на дійсність за допомогою [DOMDocument::validate](domdocument.validate.html) або `DOMDocument::validateOnParse`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання DOMAttr::isId()**

```php
<?php

$doc = new DomDocument;

// Необходимо проверить документ на действительность перед тем как ссылаться по идентификатору
$doc->validateOnParse = true;
$doc->Load('book.xml');

// Получаем атрибут элемента с именем идентификатора chapter
$attr = $doc->getElementsByTagName('chapter')->item(0)->getAttributeNode('id');

var_dump($attr->isId()); // bool(true)

?>
```