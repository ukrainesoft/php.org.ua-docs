Увімкнути або вимкнути відступи

-   [« XMLWriter::outputMemory](xmlwriter.outputmemory.html)
    
-   [XMLWriter::setIndentString »](xmlwriter.setindentstring.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Увімкнути або вимкнути відступи
    

# XMLWriter::setIndent

# xmlwritersetindent

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::setIndent -- xmlwritersetindent — Увімкнути або вимкнути відступи

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::setIndent(bool $enable): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_set_indent(XMLWriter $writer, bool $enable): bool
```

Вмикає або вимикає відступи.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`enable`

Визначає, чи додавання відступу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 **XMLWriter::setIndent()** і змішаний вміст**

Увімкнення відступу не підходить для змішаного вмісту, оскільки рядок відступу також вставляється перед вбудованими елементами.

```php
<?php
$writer = new XMLWriter();
$writer->openMemory();
$writer->setIndent(2);
$writer->startDocument();
$writer->startElement('p');
$writer->text('до');
$writer->writeElement('a', 'элемента');
$writer->text('после');
$writer->endElement();
$writer->endDocument();
echo $writer->outputMemory();
?>
```

Результат виконання цього прикладу:

```
<?xml version="1.0"?>
<p>до <a>элемена</a>
после</p>
```

### Примітки

> **Зауваження**
> 
> Відступ скидається при відкритті xmlwriter.

### Дивіться також

-   [XMLWriter::setIndentString()](xmlwriter.setindentstring.html) - Встановити рядок, який використовується для відступів