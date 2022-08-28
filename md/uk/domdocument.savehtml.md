Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML

-   [« DOMDocument::save](domdocument.save.html)
    
-   [DOMDocument::saveHTMLFile »](domdocument.savehtmlfile.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Зберігає документ із внутрішнього подання до рядка, використовуючи форматування HTML
    

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

Повертає HTML або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Збереження HTML-дерева у вигляді рядка**

```php
<?php

$doc = new DOMDocument('1.0');

$root = $doc->createElement('html');
$root = $doc->appendChild($root);

$head = $doc->createElement('head');
$head = $root->appendChild($head);

$title = $doc->createElement('title');
$title = $head->appendChild($title);

$text = $doc->createTextNode('Это заголовок');
$text = $title->appendChild($text);

echo $doc->saveHTML();

?>
```

### Дивіться також

-   [DOMDocument::saveHTMLFile()](domdocument.savehtmlfile.html) - Зберігає документ із внутрішнього подання до файлу, використовуючи форматування HTML
-   [DOMDocument::loadHTML()](domdocument.loadhtml.html) - Завантаження HTML з рядка
-   [DOMDocument::loadHTMLFile()](domdocument.loadhtmlfile.html) - Завантаження HTML із файлу