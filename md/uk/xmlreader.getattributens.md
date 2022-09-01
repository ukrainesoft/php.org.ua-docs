---
navigation:
  - xmlreader.getattributeno.md: '« XMLReader::getAttributeNo'
  - xmlreader.getparserproperty.md: 'XMLReader::getParserProperty »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::getAttributeNs'
---
# XMLReader::getAttributeNs

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::getAttributeNs — Отримати значення атрибуту по localname та URI

### Опис

```methodsynopsis
public XMLReader::getAttributeNs(string $name, string $namespace): ?string
```

Повертає значення атрибуту по імені та URI простору імен або порожній рядок, якщо атрибут не існує або не розташований на вузлі елемента.

### Список параметрів

`name`

Місцеве ім'я.

`namespace`

URI простір імен.

### Значення, що повертаються

Значення атрибуту або **`null`**, якщо атрибут із заданим `name` і `namespace` не знайдено чи немає позиції елемента.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція більше не може повертати **`false`** |

### Дивіться також

-   [XMLReader::getAttribute()](xmlreader.getattribute.md) - Отримати значення атрибуту з певним ім'ям
-   [XMLReader::getAttributeNo()](xmlreader.getattributeno.md) - Отримати значення атрибуту за індексом
