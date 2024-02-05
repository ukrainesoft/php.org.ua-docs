---
navigation:
  - xmlreader.movetonextattribute.md: '« XMLReader::moveToNextAttribute'
  - xmlreader.open.md: 'XMLReader::open »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::next

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::next — Перемістити курсор на наступний вузол, пропускаючи всі дерева.

### Опис

```methodsynopsis
public XMLReader::next(?string $name = null): bool
```

Позиціонує курсор на наступному вузлі, пропускаючи усі піддерева. Якщо такий вузол не існує, курсор переміщається до кінця документа.

### Список параметрів

`name`

Ім'я наступного вузла переходу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `name` тепер допускає значення null. |

### Дивіться також

-   [XMLReader::moveToNextAttribute()](xmlreader.movetonextattribute.md) \- Перемістити позицію курсору на наступний атрибут
-   [XMLReader::moveToElement()](xmlreader.movetoelement.md) \- Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.md) \- Перемістити курсор до атрибуту із заданим ім'ям
