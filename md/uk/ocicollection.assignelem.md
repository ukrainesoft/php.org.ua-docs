---
navigation:
  - ocicollection.assign.md: '« OCICollection::assign'
  - ocicollection.free.md: 'OCICollection::free »'
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::assignElem'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCICollection::assignElem

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCICollection::assignElem — Надає значення елементу колекції

### Опис

```methodsynopsis
public OCICollection::assignElem(int $index, string $value): bool
```

Надає значення елементу колекції з індексом `index`

### Список параметрів

`index`

Індекс елемент. Перший індекс – нуль.

`value`

Може бути рядком чи числом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Collection**перейменований на[OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::getElem](ocicollection.getelem.md)
