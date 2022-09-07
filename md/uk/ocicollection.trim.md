---
navigation:
  - ocicollection.size.md: '« OCICollection::size'
  - class.ocilob.md: OCILob »
  - index.md: PHP Manual
  - class.ocicollection.md: OCICollection
title: 'OCICollection::trim'
---
# OCICollection::trim

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Collection** перейменований на [OCICollection](class.ocicollection.md) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::size](ocicollection.size.md)
