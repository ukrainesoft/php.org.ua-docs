---
navigation:
  - domdocument.createdocumentfragment.md: '« DOMDocument::createDocumentFragment'
  - domdocument.createelementns.md: 'DOMDocument::createElementNS »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createElement'
---
# DOMDocument::createElement

(PHP 5, PHP 7, PHP 8)

DOMDocument::createElement — Створити новий вузол елемента

### Опис

```methodsynopsis
public DOMDocument::createElement(string $localName, string $value = ""): DOMElement|false
```

Ця функція створює екземпляр класу [DOMElement](class.domelement.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`localName`

Ім'я тег елемент.

`value`

Значення елемента. За промовчанням буде створено порожній елемент. Значення може бути встановлене пізніше за допомогою [DOMElement::$nodeValue](class.domnode.html#domnode.props.nodevalue)

Значення використовується дослівно, крім < і >, які будуть екрановані. Зверніть увагу, що & має бути екранований самостійно, інакше він буде розглядатися як початок посилання на сутність. Також не буде екранований.

### Значення, що повертаються

Повертає новий об'єкт класу [DOMElement](class.domelement.md) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `localName` містить неприпустимі символи.

### Приклади

**Приклад #1 Створення нового елемента та вставка його як кореневий**

```php
<?php

$dom = new DOMDocument('1.0', 'utf-8');

$element = $dom->createElement('test', 'Это корневой элемент!');

// Вставляем новый элемент как корень (потомок документа)
$dom->appendChild($element);

echo $dom->saveXML();
?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<test>Это корневой элемент!</test>
```

**Приклад #2 Надсилання тексту, що містить неекранований & в `value`**

```php
<?php
$dom = new DOMDocument('1.0', 'utf-8');
$element = $dom->createElement('foo', 'я & ты');
$dom->appendChild($element);
echo $dom->saveXML();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Warning: DOMDocument::createElement(): unterminated entity reference             you in /in/BjTCg on line 4
<?xml version="1.0" encoding="utf-8"?>
<foo/>
```

### Примітки

> **Зауваження**
> 
> Значення `value` *не* буде екрановано. Використовуйте функцію [DOMDocument::createTextNode()](domdocument.createtextnode.md) для створення текстового вузла з *підтримкою екранування*

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) - створити новий фрагмент документа
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол
