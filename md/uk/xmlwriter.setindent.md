---
navigation:
  - xmlwriter.outputmemory.md: '« XMLWriter::outputMemory'
  - xmlwriter.setindentstring.md: 'XMLWriter::setIndentString »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::setIndent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::setIndent

# xmlwriter\_set\_indent

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::setIndent -- xmlwriter\_set\_indent — Увімкнути або вимкнути відступи

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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`enable`

Визначає, чи додавання відступу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Приклади

**Пример #1**XMLWriter::setIndent()\*\* і змішаний вміст\*\*

Увімкнення відступу не підходить для змішаного вмісту, оскільки рядок відступу також вставляється перед вбудованими елементами.

```php
<?php
$writer = new XMLWriter();
$writer->openMemory();
$writer->setIndent(2);
$writer->startDocument();
$writer->startElement('p');
$writer->text('до');
$writer->writeElement('a', 'элемента');
$writer->text('после');
$writer->endElement();
$writer->endDocument();
echo $writer->outputMemory();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<p>до <a>элемена</a>
после</p>
```

### Примітки

> **Зауваження** :
> 
> Відступ скидається при відкритті xmlwriter.

### Дивіться також

-   [XMLWriter::setIndentString()](xmlwriter.setindentstring.md) \- Встановити рядок, який використовується для відступів
