---
navigation:
  - domdocument.savehtml.md: '« DOMDocument::saveHTML'
  - domdocument.savexml.md: 'DOMDocument::saveXML »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::saveHTMLFile'
---
# DOMDocument::saveHTMLFile

(PHP 5, PHP 7, PHP 8)

DOMDocument::saveHTMLFile — Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML

### Опис

```methodsynopsis
public DOMDocument::saveHTMLFile(string $filename): int|false
```

Створює HTML-документ із DOM-подання. Цю функцію зазвичай викликають після побудови нового документа DOM, як показано в прикладі нижче.

### Список параметрів

`filename`

Шлях до файлу, до якого збережеться HTML-документ.

### Значення, що повертаються

Повертає кількість записаних байт або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Збереження HTML-дерева у файл**

```php
<?php

$doc = new DOMDocument('1.0');
// мы хотим красивый вывод
$doc->formatOutput = true;

$root = $doc->createElement('html');
$root = $doc->appendChild($root);

$head = $doc->createElement('head');
$head = $root->appendChild($head);

$title = $doc->createElement('title');
$title = $head->appendChild($title);

$text = $doc->createTextNode('Это заголовок');
$text = $title->appendChild($text);

echo 'Записано: ' . $doc->saveHTMLFile("/tmp/test.html") . ' байт'; // Записано: 129 байт

?>
```

### Дивіться також

-   [DOMDocument::saveHTML()](domdocument.savehtml.md) - Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
-   [DOMDocument::loadHTML()](domdocument.loadhtml.md) - Завантаження HTML з рядка
-   [DOMDocument::loadHTMLFile()](domdocument.loadhtmlfile.md) - Завантаження HTML із файлу
