---
navigation:
  - xmlreader.movetofirstattribute.md: '« XMLReader::moveToFirstAttribute'
  - xmlreader.next.md: 'XMLReader::next »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::moveToNextAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::moveToNextAttribute

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::moveToNextAttribute — Перемістити позицію курсору на наступний атрибут

### Опис

```methodsynopsis
public XMLReader::moveToNextAttribute(): bool
```

Переміщує курсор до наступного атрибута, якщо курсор спозиційований на атрибуті або переміщує позицію на перший атрибут, якщо спозиціоновано на елементі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [XMLReader::moveToElement()](xmlreader.movetoelement.md) \- Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.md) \- Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::moveToAttributeNo()](xmlreader.movetoattributeno.md) \- Перемістити курсор на атрибут за індексом
-   [XMLReader::moveToAttributeNs()](xmlreader.movetoattributens.md) \- Перемістити курсор до іменованого атрибуту
-   [XMLReader::moveToFirstAttribute()](xmlreader.movetofirstattribute.md) \- Перемістити позицію курсору на перший атрибут
