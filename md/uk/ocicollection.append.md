---
navigation:
  - class.ocicollection.md: « OCICollection
  - ocicollection.assign.md: 'OCICollection::assign »'
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::append'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCICollection::append

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCICollection::append — Додає елемент до колекції

### Опис

```methodsynopsis
public OCICollection::append(string $value): bool
```

Додає елемент до кінця колекції.

### Список параметрів

`value`

Значення, яке додається до кінця колекції.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Collection**перейменований на[OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::assign](ocicollection.assign.md)
