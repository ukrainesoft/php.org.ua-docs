---
navigation:
  - domdocument.replacechildren.md: '« DOMDocument::replaceChildren'
  - domdocument.savehtml.md: 'DOMDocument::saveHTML »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::save'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::save

(PHP 5, PHP 7, PHP 8)

DOMDocument::save — Зберігає XML-дерево з внутрішнього подання до файлу

### Опис

```methodsynopsis
public DOMDocument::save(string $filename, int $options = 0): int|false
```

Створює XML-документ із подання DOM. Цю функцію зазвичай викликають після побудови нового документа DOM, як показано в прикладі нижче.

### Список параметрів

`filename`

Шлях до файлу, в який буде збережено документ XML.

`options`

Додаткові налаштування. На даний момент підтримується тільки [LIBXML\_NOEMPTYTAG](libxml.constants.md)

### Значення, що повертаються

Повертає кількість записаних байт або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Збереження DOM-дерева у файл**

```php
<?php

$doc = new DOMDocument('1.0');
// мы хотим красивый вывод
$doc->formatOutput = true;

$root = $doc->createElement('book');
$root = $doc->appendChild($root);

$title = $doc->createElement('title');
$title = $root->appendChild($title);

$text = $doc->createTextNode('This is the title');
$text = $title->appendChild($text);

echo 'Записано: ' . $doc->save("/tmp/test.xml") . ' байт'; // Записано: 72 байт

?>
```

### Дивіться також

-   [DOMDocument::saveXML()](domdocument.savexml.md) \- Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
-   [DOMDocument::load()](domdocument.load.md) \- Завантаження XML із файлу
-   [DOMDocument::loadXML()](domdocument.loadxml.md) \- Завантаження XML з рядка
