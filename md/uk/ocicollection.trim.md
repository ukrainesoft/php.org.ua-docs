---
navigation:
  - ocicollection.size.md: '« OCICollection::size'
  - class.ocilob.md: OCILob »
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::trim'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCICollection::trim

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCICollection::trim — Відсікає елементи з кінця колекції

### Опис

```methodsynopsis
public OCICollection::trim(int $num): bool
```

Відсікає `num` елементів з кінця колекції.

### Список параметрів

`num`

Кількість елементів для відсікання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Collection**перейменований на[OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::size](ocicollection.size.md)
