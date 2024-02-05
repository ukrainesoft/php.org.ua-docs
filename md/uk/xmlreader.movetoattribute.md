---
navigation:
  - xmlreader.lookupnamespace.md: '« XMLReader::lookupNamespace'
  - xmlreader.movetoattributeno.md: 'XMLReader::moveToAttributeNo »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::moveToAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::moveToAttribute

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::moveToAttribute — Перемістити курсор до атрибуту із заданим ім'ям

### Опис

```methodsynopsis
public XMLReader::moveToAttribute(string $name): bool
```

Позиціонує курсор на атрибуті із заданим ім'ям.

### Список параметрів

`name`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [XMLReader::moveToElement()](xmlreader.movetoelement.md) \- Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttributeNo()](xmlreader.movetoattributeno.md) \- Перемістити курсор на атрибут за індексом
-   [XMLReader::moveToAttributeNs()](xmlreader.movetoattributens.md) \- Перемістити курсор до іменованого атрибуту
-   [XMLReader::moveToFirstAttribute()](xmlreader.movetofirstattribute.md) \- Перемістити позицію курсору на перший атрибут
