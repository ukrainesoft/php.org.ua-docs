---
navigation:
  - xmlreader.open.md: '« XMLReader::open'
  - xmlreader.readinnerxml.md: 'XMLReader::readInnerXml »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::read

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::read — Переміститися до наступного сайту в документі

### Опис

```methodsynopsis
public XMLReader::read(): bool
```

Переміщує курсор до наступного вузла документа.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [XMLReader::moveToElement()](xmlreader.movetoelement.md) \- Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.md) \- Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::next()](xmlreader.next.md) \- Перемістити курсор на наступний вузол, пропускаючи всі піддерева
