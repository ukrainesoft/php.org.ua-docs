---
navigation:
  - xmlreader.expand.md: '« XMLReader::expand'
  - xmlreader.getattributeno.md: 'XMLReader::getAttributeNo »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::getAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::getAttribute

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::getAttribute — Отримати значення атрибуту з певним ім'ям

### Опис

```methodsynopsis
public XMLReader::getAttribute(string $name): ?string
```

Возвращает значение именованного атрибута или\*\*`null`\*\*якщо атрибут не існує або не знаходиться у вузлі елемента.

### Список параметрів

`name`

Ім'я атрибуту.

### Значення, що повертаються

Значение атрибута или\*\*`null`\*\*, якщо атрибут із заданим параметром `name` не знайдено чи немає позиції елемента.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не може повертати **`false`** |

### Дивіться також

-   [XMLReader::getAttributeNo()](xmlreader.getattributeno.md) \- Отримати значення атрибуту за індексом
-   [XMLReader::getAttributeNs()](xmlreader.getattributens.md) \- Отримати значення атрибуту по localname та URI
