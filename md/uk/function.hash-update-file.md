---
navigation:
  - function.hash-pbkdf2.html: « hashpbkdf2
  - function.hash-update-stream.html: hashupdatestream »
  - index.html: PHP Manual
  - ref.hash.html: Функции Hash
title: hashupdatefile
---
# hashupdatefile

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashupdatefile — Додає дані з файлу до активного контексту хешування

### Опис

```methodsynopsis
hash_update_file(HashContext $context, string $filename, ?resource $stream_context = null): bool
```

### Список параметрів

`context`

Контекст хешування, повернутий [hashinit()](function.hash-init.html)

`filename`

Ім'я або URL-файл для хешування; Підтримуються обробники Fopen.

`stream_context`

Контекст потоку, повернутий [streamcontextcreate()](function.stream-context-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `stream_context` тепер допускає значення null. |
|  | Приймає [HashContext](class.hashcontext.html), а чи не ресурс. |

### Дивіться також

-   [hashinit()](function.hash-init.html) - Ініціалізація інкрементального контексту хешування
-   [hashupdate()](function.hash-update.html) - Додає дані до активного контексту хешування
-   [hashupdatestream()](function.hash-update-stream.html) - Додає дані з відкритого потоку до активного контексту хешування
-   [hashfinal()](function.hash-final.html) - Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
-   [hash()](function.hash.html) - Генерує хеш-код (підпис повідомлення)
-   [hashfile()](function.hash-file.html) - Генерація хеш-значення, використовуючи вміст заданого файлу
