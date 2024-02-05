---
navigation:
  - function.hash-pbkdf2.md: « hash\_pbkdf2
  - function.hash-update-stream.md: hash\_update\_stream »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_update\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_update\_file

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_update\_file — Додає дані з файлу до активного контексту хешування

### Опис

```methodsynopsis
hash_update_file(HashContext $context, string $filename, ?resource $stream_context = null): bool
```

### Список параметрів

`context`

Контекст хешування, повернутий [hash\_init()](function.hash-init.md)

`filename`

Ім'я або URL-файл для хешування; Підтримуються обробники Fopen.

`stream_context`

Контекст потоку, повернутий [stream\_context\_create()](function.stream-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `stream_context` тепер допускає значення null. |
| 7.2.0 | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Дивіться також

-   [hash\_init()](function.hash-init.md) \- Ініціалізація інкрементального контексту хешування
-   [hash\_update()](function.hash-update.md) \- Додає дані до активного контексту хешування
-   [hash\_update\_stream()](function.hash-update-stream.md) \- Додає дані з відкритого потоку до активного контексту хешування
-   [hash\_final()](function.hash-final.md) \- Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
-   [hash()](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
-   [hash\_file()](function.hash-file.md) \- Генерація хеш-значення, використовуючи вміст заданого файлу
