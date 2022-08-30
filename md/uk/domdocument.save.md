Зберігає XML-дерево з внутрішнього подання до файлу

-   [« DOMDocument::relaxNGValidateSource](domdocument.relaxngvalidatesource.html)
    
-   [DOMDocument::saveHTML »](domdocument.savehtml.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Зберігає XML-дерево з внутрішнього подання до файлу
    

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

Додаткові налаштування. На даний момент підтримується тільки [LIBXMLNOEMPTYTAG](libxml.constants.html)

### Значення, що повертаються

Повертає кількість записаних байт або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Збереження DOM-дерева у файл**

```php
<?php

$doc = new DOMDocument('1.0');
// мы хотим красивый вывод
$doc->formatOutput = true;

$root = $doc->createElement('book');
$root = $doc->appendChild($root);

$title = $doc->createElement('title');
$title = $root->appendChild($title);

$text = $doc->createTextNode('This is the title');
$text = $title->appendChild($text);

echo 'Записано: ' . $doc->save("/tmp/test.xml") . ' байт'; // Записано: 72 байт

?>
```

### Дивіться також

-   [DOMDocument::saveXML()](domdocument.savexml.html) - Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
-   [DOMDocument::load()](domdocument.load.html) - Завантаження XML із файлу
-   [DOMDocument::loadXML()](domdocument.loadxml.html) - Завантаження XML з рядка