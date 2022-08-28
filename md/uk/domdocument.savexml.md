Зберігає XML-дерево з внутрішньої вистави у вигляді рядка

-   [« DOMDocument::saveHTMLFile](domdocument.savehtmlfile.html)
    
-   [DOMDocument::schemaValidate »](domdocument.schemavalidate.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Зберігає XML-дерево з внутрішньої вистави у вигляді рядка
    

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

Додаткові налаштування. На даний момент підтримується тільки [LIBXML\_NOEMPTYTAG](libxml.constants.html)

### Значення, що повертаються

Повертає XML або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо `node` належить іншому документу.

### Приклади

**Приклад #1 Збереження DOM-дерева у вигляді рядка**

```php
<?php

$doc = new DOMDocument('1.0');
// мы хотим красивый вывод
$doc->formatOutput = true;

$root = $doc->createElement('book');
$root = $doc->appendChild($root);

$title = $doc->createElement('title');
$title = $root->appendChild($title);

$text = $doc->createTextNode('Это заголовок');
$text = $title->appendChild($text);

echo "Сохранение всего документа:\n";
echo $doc->saveXML() . "\n";

echo "Сохранение только заголовка:\n";
echo $doc->saveXML($title);

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

-   [DOMDocument::save()](domdocument.save.html) - Зберігає XML-дерево із внутрішнього подання до файлу
-   [DOMDocument::load()](domdocument.load.html) - Завантаження XML із файлу
-   [DOMDocument::loadXML()](domdocument.loadxml.html) - Завантаження XML з рядка