---
navigation:
  - function.hash-update-stream.md: « hash\_update\_stream
  - function.hash.md: hash »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_update
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_update

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_update — Додає дані до активного контексту хешування

### Опис

```methodsynopsis
hash_update(HashContext $context, string $data): bool
```

### Список параметрів

`context`

Контекст хешування, що повертається [hash\_init()](function.hash-init.md)

`data`

Повідомлення, яке має бути включене до хеша.

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Дивіться також

-   [hash\_init()](function.hash-init.md) \- Ініціалізація інкрементального контексту хешування
-   [hash\_update\_file()](function.hash-update-file.md) \- Додає дані з файлу до активного контексту хешування
-   [hash\_update\_stream()](function.hash-update-stream.md) \- Додає дані з відкритого потоку до активного контексту хешування
-   [hash\_final()](function.hash-final.md) \- Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
