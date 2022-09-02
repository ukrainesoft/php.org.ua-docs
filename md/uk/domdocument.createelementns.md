---
navigation:
  - domdocument.createelement.md: '« DOMDocument::createElement'
  - domdocument.createentityreference.md: 'DOMDocument::createEntityReference »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createElementNS'
---
# DOMDocument::createElementNS

(PHP 5, PHP 7, PHP 8)

DOMDocument::createElementNS — Створити новий вузол елемента з відповідним простором імен

### Опис

```methodsynopsis
public DOMDocument::createElementNS(?string $namespace, string $qualifiedName, string $value = ""): DOMElement|false
```

Ця функція створює новий вузол-елемент із відповідним простором імен. Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`namespace`

URI простір імен.

`qualifiedName`

Кваліфіковане ім'я елемента у вигляді `prefix:tagname`

`value`

Значення елемента. За промовчанням буде створено порожній елемент. Задати значення також можна пізніше за допомогою [DOMElement::$nodeValue](class.domnode.md#domnode.props.nodevalue)

### Значення, що повертаються

Новий об'єкт класу [DOMElement](class.domelement.md) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `qualifiedName` містить неприпустимі символи.

**`DOM_NAMESPACE_ERR`**

Виникає, якщо `qualifiedName` не правильно сформовано.

### Приклади

**Приклад #1 Створення елемента та вставка в документ як кореневий**

```php
<?php

$dom = new DOMDocument('1.0', 'utf-8');

$element = $dom->createElementNS('http://www.example.com/XFoo', 'xfoo:test', 'Это корневой элемент!');

// Вставляем новый элемент как корень (потомок документа)
$dom->appendChild($element);

echo $dom->saveXML();
?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<xfoo:test xmlns:xfoo="http://www.example.com/XFoo">Это корневой элемент!</xfoo:test>
```

**Приклад #2 Приклад префіксу простору імен**

```php
<?php
$doc  = new DOMDocument('1.0', 'utf-8');
$doc->formatOutput = true;
$root = $doc->createElementNS('http://www.w3.org/2005/Atom', 'element');
$doc->appendChild($root);
$root->setAttributeNS('http://www.w3.org/2000/xmlns/' ,'xmlns:g', 'http://base.google.com/ns/1.0');
$item = $doc->createElementNS('http://base.google.com/ns/1.0', 'g:item_type', 'house');
$root->appendChild($item);

echo $doc->saveXML(), "\n";

echo $item->namespaceURI, "\n"; // Выведет: http://base.google.com/ns/1.0
echo $item->prefix, "\n";       // Выведет: g
echo $item->localName, "\n";    // Выведет: item_type
?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<element xmlns="http://www.w3.org/2005/Atom" xmlns:g="http://base.google.com/ns/1.0">
  <g:item_type>house</g:item_type>
</element>

http://base.google.com/ns/1.0
g
item_type
```

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол
