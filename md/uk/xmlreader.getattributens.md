---
navigation:
  - xmlreader.getattributeno.md: '« XMLReader::getAttributeNo'
  - xmlreader.getparserproperty.md: 'XMLReader::getParserProperty »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::getAttributeNs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::getAttributeNs

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::getAttributeNs — Отримати значення атрибуту по localname та URI

### Опис

```methodsynopsis
public XMLReader::getAttributeNs(string $name, string $namespace): ?string
```

Повертає значення атрибуту на ім'я та URI простору імен або порожній рядок, якщо атрибут не існує або не розташований на вузлі елемента.

### Список параметрів

`name`

Місцеве ім'я.

`namespace`

URI простір імен.

### Значення, що повертаються

Значение атрибута или\*\*`null`\*\*, якщо атрибут із заданим `name`и`namespace` не знайдено чи немає позиції елемента.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не може повертати **`false`** |

### Дивіться також

-   [XMLReader::getAttribute()](xmlreader.getattribute.md) \- Отримати значення атрибута з певним ім'ям
-   [XMLReader::getAttributeNo()](xmlreader.getattributeno.md) \- Отримати значення атрибуту за індексом
