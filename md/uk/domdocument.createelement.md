---
navigation:
  - domdocument.createdocumentfragment.md: '« DOMDocument::createDocumentFragment'
  - domdocument.createelementns.md: 'DOMDocument::createElementNS »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createElement'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createElement

(PHP 5, PHP 7, PHP 8)

DOMDocument::createElement — Створює новий вузол елемента

### Опис

```methodsynopsis
public DOMDocument::createElement(string $localName, string $value = ""): DOMElement|false
```

Ця функція створює екземпляр класу [DOMElement](class.domelement.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`localName`

Ім'я тег елемент.

`value`

Значення елемента. За промовчанням буде створено порожній елемент. Значення також може бути встановлене пізніше шляхом присвоювання при прямому зверненні до властивості [DOMElement::$nodeValue](class.domnode.md#domnode.props.nodevalue)

Значення буде встановлено дослівно, крім символів < і >, які будуть екрановані. Зверніть увагу, що символ & потрібно екранувати самому, інакше він розглядатиметься як початок посилання на суть. Символ кавчок також не буде екранований.

### Значення, що повертаються

Повертає новий об'єкт класу [DOMElement](class.domelement.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо параметр `localName` містить неприпустимі символи.

### Приклади

**Приклад #1 Створення нового елемента та вставка його як кореневий**

```php
<?php

$dom = new DOMDocument('1.0', 'utf-8');

$element = $dom->createElement('test', 'Это корневой элемент!');

// Вставляем новый элемент как корень (потомок документа)
$dom->appendChild($element);

echo $dom->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0" encoding="utf-8"?>
<test>Это корневой элемент!</test>
```

**Приклад #2 Надсилання тексту, що містить неекранований & в `value`**

```php
<?php
$dom = new DOMDocument('1.0', 'utf-8');
$element = $dom->createElement('foo', 'я & ты');
$dom->appendChild($element);
echo $dom->saveXML();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Warning: DOMDocument::createElement(): unterminated entity reference             you in /in/BjTCg on line 4
<?xml version="1.0" encoding="utf-8"?>
<foo/>
```

### Примітки

> **Зауваження** :
> 
> Значение`value` *не* буде екрановано. Використовуйте функцію [DOMDocument::createTextNode()](domdocument.createtextnode.md) для створення текстового вузла з *підтримкою екранування*

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) \- Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) \- Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
