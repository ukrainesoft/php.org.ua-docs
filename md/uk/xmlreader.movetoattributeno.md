---
navigation:
  - xmlreader.movetoattribute.md: '« XMLReader::moveToAttribute'
  - xmlreader.movetoattributens.md: 'XMLReader::moveToAttributeNs »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::moveToAttributeNo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::moveToAttributeNo

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::moveToAttributeNo — Перемістити курсор на атрибут за індексом

### Опис

```methodsynopsis
public XMLReader::moveToAttributeNo(int $index): bool
```

Встановлює курсор на атрибуті, виходячи з його позиції.

### Список параметрів

`index`

Позиція атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [XMLReader::moveToElement()](xmlreader.movetoelement.md) \- Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.md) \- Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::moveToAttributeNs()](xmlreader.movetoattributens.md) \- Перемістити курсор до іменованого атрибуту
-   [XMLReader::moveToFirstAttribute()](xmlreader.movetofirstattribute.md) \- Перемістити позицію курсору на перший атрибут
