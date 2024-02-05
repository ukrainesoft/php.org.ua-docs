---
navigation:
  - xmlwriter.setindent.md: '« XMLWriter::setIndent'
  - xmlwriter.startattribute.md: 'XMLWriter::startAttribute »'
  - index.md: PHP Manual
  - class.xmlwriter.md: XMLWriter
title: 'XMLWriter::setIndentString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLWriter::setIndentString

# xmlwriter\_set\_indent\_string

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::setIndentString -- xmlwriter\_set\_indent\_string — Встановити рядок, який використовується для відступів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::setIndentString(string $indentation): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_set_indent_string(XMLWriter $writer, string $indentation): bool
```

Встановлює рядок, який буде використовуватися для відступу кожного елемента/атрибута в XML.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.md) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.md)

`indentString`

Відступ рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | В параметре`writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Примітки

> **Зауваження** :
> 
> Відступ скидається при відкритті xmlwriter.

### Дивіться також

-   [XMLWriter::setIndent()](xmlwriter.setindent.md) \- Увімкнути або вимкнути відступи
