---
navigation:
  - xmlreader.movetoattributens.md: '« XMLReader::moveToAttributeNs'
  - xmlreader.movetofirstattribute.md: 'XMLReader::moveToFirstAttribute »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::moveToElement'
---
# XMLReader::moveToElement

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::moveToElement — Позиціонувати курсор на батьківському елементі поточного атрибуту

### Опис

```methodsynopsis
public XMLReader::moveToElement(): bool
```

Переміщує курсор до батьківського елемента поточного атрибута.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання та **`false`** у разі невдачі або якщо неможливо виконати позиціонування курсору на атрибуті, коли цей метод викликається.

### Дивіться також

-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.md) - Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::moveToAttributeNo()](xmlreader.movetoattributeno.md) - Перемістити курсор на атрибут за індексом
-   [XMLReader::moveToAttributeNs()](xmlreader.movetoattributens.md) - Перемістити курсор до іменованого атрибуту
-   [XMLReader::moveToFirstAttribute()](xmlreader.movetofirstattribute.md) - Перемістити позицію курсору на перший атрибут
