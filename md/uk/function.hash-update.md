---
navigation:
  - function.hash-update-stream.md: « hashupdatestream
  - function.hash.md: hash »
  - index.md: PHP Manual
  - ref.hash.md: Функции Hash
title: hashupdate
---
# hashupdate

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashupdate — Додає дані до активного контексту хешування

### Опис

```methodsynopsis
hash_update(HashContext $context, string $data): bool
```

### Список параметрів

`context`

Контекст хешування, що повертається [hashinit()](function.hash-init.md)

`data`

Повідомлення, яке має бути включене до хеша.

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Дивіться також

-   [hashinit()](function.hash-init.md) - Ініціалізація інкрементального контексту хешування
-   [hashupdatefile()](function.hash-update-file.md) - Додає дані з файлу до активного контексту хешування
-   [hashupdatestream()](function.hash-update-stream.md) - Додає дані з відкритого потоку до активного контексту хешування
-   [hashfinal()](function.hash-final.md) - Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
