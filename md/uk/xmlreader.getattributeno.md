---
navigation:
  - xmlreader.getattribute.md: '« XMLReader::getAttribute'
  - xmlreader.getattributens.md: 'XMLReader::getAttributeNs »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::getAttributeNo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::getAttributeNo

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::getAttributeNo — Отримати значення атрибута за індексом

### Опис

```methodsynopsis
public XMLReader::getAttributeNo(int $index): ?string
```

Повертає значення атрибута на основі позиції або порожній рядок, якщо атрибут не існує або не розташований на вузлі елемента.

### Список параметрів

`index`

Позиція атрибуту.

### Значення, що повертаються

Значение атрибута или\*\*`null`\*\*, якщо атрибут із заданим параметром `index` не існує чи ні позиції елемента.

### Дивіться також

-   [XMLReader::getAttribute()](xmlreader.getattribute.md) \- Отримати значення атрибута з певним ім'ям
-   [XMLReader::getAttributeNs()](xmlreader.getattributens.md) \- Отримати значення атрибуту по localname та URI
