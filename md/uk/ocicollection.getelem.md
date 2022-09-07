---
navigation:
  - ocicollection.free.md: '« OCICollection::free'
  - ocicollection.max.md: 'OCICollection::max »'
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::getElem'
---
# OCICollection::getElem

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCICollection::getElem — Повертає значення елемента

### Опис

```methodsynopsis
public OCICollection::getElem(int $index): string|float|null|false
```

Повертає значення елемента з індексом `index` (починаючи з нуля).

### Список параметрів

`index`

Індекс елемент. Перший індекс – нуль.

### Значення, що повертаються

Djpdhfoftn \*\*`false`\*\*якщо такого елемента немає; \*\*`null`\*\*якщо елемент дорівнює **`null`**; рядок, якщо елемент відноситься до рядкового стовпця, та число, якщо елемент є числовим полем.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Collection** перейменований на [OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::assignElem](ocicollection.assignelem.md)
