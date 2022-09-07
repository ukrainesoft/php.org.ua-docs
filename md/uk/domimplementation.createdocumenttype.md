---
navigation:
  - domimplementation.createdocument.md: '« DOMImplementation::createDocument'
  - domimplementation.hasfeature.md: 'DOMImplementation::hasFeature »'
  - index.md: PHP Manual
  - class.domimplementation.md: DOMImplementation
title: 'DOMImplementation::createDocumentType'
---
# DOMImplementation::createDocumentType

(PHP 5, PHP 7, PHP 8)

DOMImplementation::createDocumentType — Створює порожній об'єкт класу DOMDocumentType

### Опис

```methodsynopsis
public DOMImplementation::createDocumentType(string $qualifiedName, string $publicId = "", string $systemId = ""): DOMDocumentType|false
```

Створює порожній об'єкт класу [DOMDocumentType](class.domdocumenttype.md). Оголошення сутності та позначення будуть недоступні. Посилання на сутності не замінятимуться і додавання атрибутів за умовчанням не відбуватиметься.

### Список параметрів

`qualifiedName`

Кваліфікована назва типу документа для створення.

`publicId`

Загальнодоступний ідентифікатор зовнішнього підмножини.

`systemId`

Системний ідентифікатор зовнішнього підмножини.

### Значення, що повертаються

Новий об'єкт класу [DOMDocumentType](class.domdocumenttype.md) з атрибутом `ownerDocument`, встановленим у **`null`**

### Помилки

**`DOM_NAMESPACE_ERR`**

Виникає, якщо виявлена ​​помилка у рядку `qualifiedName`

До PHP 8.0.0 метод *може* викликатись статично, але викличе помилку **`E_DEPRECATED`**. Починаючи з PHP 8.0.0, виклик цього методу статично викидає виняток [Error](class.error.md)

### Приклади

**Приклад #1 Створення документа із прикріпленим DTD**

```php
<?php

// Создаёт экземпляр класса DOMImplementation
$imp = new DOMImplementation;

// Создаёт экземпляр класса DOMDocumentType
$dtd = $imp->createDocumentType('graph', '', 'graph.dtd');

// Создаёт объект DOMDocument
$dom = $imp->createDocument("", "", $dtd);

// Установка других параметров
$dom->encoding = 'UTF-8';
$dom->standalone = false;

// Создание пустого элемента
$element = $dom->createElement('graph');

// Добавление элемента
$dom->appendChild($element);

// Получение и печать документа
echo $dom->saveXML();

?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<!DOCTYPE graph SYSTEM "graph.dtd">
<graph/>
```

### Дивіться також

-   [DOMImplementation::createDocument()](domimplementation.createdocument.md) - Створює об'єкт класу DOMDocument заданого типу з його елементом
