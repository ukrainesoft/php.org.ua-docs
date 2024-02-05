---
navigation:
  - domdocument.save.md: '« DOMDocument::save'
  - domdocument.savehtmlfile.md: 'DOMDocument::saveHTMLFile »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::saveHTML'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::saveHTML

(PHP 5, PHP 7, PHP 8)

DOMDocument::saveHTML — Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML

### Опис

```methodsynopsis
public DOMDocument::saveHTML(?DOMNode $node = null): string|false
```

Створює HTML-документ із подання DOM. Цю функцію зазвичай викликають після побудови нового документа DOM, як показано в прикладі нижче.

### Список параметрів

`node`

Необов'язковий аргумент для виведення підмножини документа.

### Значення, що повертаються

Повертає HTML або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Збереження HTML-дерева у вигляді рядка**

```php
<?php

$doc = new DOMDocument('1.0');

$root = $doc->createElement('html');
$root = $doc->appendChild($root);

$head = $doc->createElement('head');
$head = $root->appendChild($head);

$title = $doc->createElement('title');
$title = $head->appendChild($title);

$text = $doc->createTextNode('Это заголовок');
$text = $title->appendChild($text);

echo $doc->saveHTML();

?>
```

### Дивіться також

-   [DOMDocument::saveHTMLFile()](domdocument.savehtmlfile.md) \- Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML
-   [DOMDocument::loadHTML()](domdocument.loadhtml.md) \- Завантаження HTML з рядка
-   [DOMDocument::loadHTMLFile()](domdocument.loadhtmlfile.md) \- Завантаження HTML із файлу
