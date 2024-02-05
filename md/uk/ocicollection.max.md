---
navigation:
  - ocicollection.getelem.md: '« OCICollection::getElem'
  - ocicollection.size.md: 'OCICollection::size »'
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::max'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCICollection::max

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCICollection::max — Повертає максимальну кількість елементів у колекції

### Опис

```methodsynopsis
public OCICollection::max(): int|false
```

Повертає максимальну кількість елементів у колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає максимальну кількість як ціле число або \*\*`false`\*\*в случае возникновения ошибки.

Якщо буде повернено 0, кількість елементів не обмежена.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Collection**перейменований на[OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::size](ocicollection.size.md)
