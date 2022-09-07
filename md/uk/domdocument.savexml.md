---
navigation:
  - domdocument.savehtmlfile.md: '« DOMDocument::saveHTMLFile'
  - domdocument.schemavalidate.md: 'DOMDocument::schemaValidate »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::saveXML'
---
# DOMDocument::saveXML

(PHP 5, PHP 7, PHP 8)

DOMDocument::saveXML — Зберігає XML-дерево з внутрішнього подання у вигляді рядка

### Опис

```methodsynopsis
public DOMDocument::saveXML(?DOMNode $node = null, int $options = 0): string|false
```

Створює XML-документ із подання DOM. Цю функцію зазвичай викликають після побудови нового документа DOM, як показано в прикладі нижче.

### Список параметрів

`node`

Використовуйте цей аргумент для виведення лише певного вузла без оголошення XML, а не всього документа.

`options`

Додаткові налаштування. На даний момент підтримується тільки [LIBXMLNOEMPTYTAG](libxml.constants.md)

### Значення, що повертаються

Повертає XML або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо `node` належить іншому документу.

### Приклади

**Приклад #1 Збереження DOM-дерева у вигляді рядка**

```php
<?php

$doc = new DOMDocument('1.0');
// мы хотим красивый вывод
$doc->formatOutput = true;

$root = $doc->createElement('book');
$root = $doc->appendChild($root);

$title = $doc->createElement('title');
$title = $root->appendChild($title);

$text = $doc->createTextNode('Это заголовок');
$text = $title->appendChild($text);

echo "Сохранение всего документа:\n";
echo $doc->saveXML() . "\n";

echo "Сохранение только заголовка:\n";
echo $doc->saveXML($title);

?>
```

Результат виконання цього прикладу:

```
Сохранение всего документа:
<?xml version="1.0"?>
<book>
  <title>Это заголовок</title>
</book>

Сохранение только заголовка:
<title>Это заголовок</title>
```

### Дивіться також

-   [DOMDocument::save()](domdocument.save.md) - Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::load()](domdocument.load.md) - Завантаження XML із файлу
-   [DOMDocument::loadXML()](domdocument.loadxml.md) - Завантаження XML з рядка
