---
navigation:
  - ocicollection.append.md: '« OCICollection::append'
  - ocicollection.assignelem.md: 'OCICollection::assignElem »'
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::assign'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCICollection::assign

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCICollection::assign — Надає колекції значення іншої, вже існуючої колекції

### Опис

```methodsynopsis
public OCICollection::assign(OCICollection $from): bool
```

Надає колекції значення іншої, раніше створеної колекції. Обидві колекції мають бути створені раніше за допомогою [oci\_new\_collection()](function.oci-new-collection.md)

### Список параметрів

`from`

Примірник OCI-Collection.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Collection**перейменований на[OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::append](ocicollection.append.md)
