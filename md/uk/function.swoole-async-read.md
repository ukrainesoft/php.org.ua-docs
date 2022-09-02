---
navigation:
  - function.swoole-async-dns-lookup.md: « swooleasyncdnslookup
  - function.swoole-async-readfile.md: swooleasyncreadfile »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функции Swoole
title: swooleasyncread
---
# swooleasyncread

(PECL swoole >= 1.9.0)

swooleasyncread — Асинхронне читання потоку файлу

### Опис

```methodsynopsis
swoole_async_read(    string $filename,    callable $callback,    int $chunk_size = 65536,    int $offset = 0): bool
```

### Список параметрів

`filename`

Ім'я файлу для читання.

`callback`

```methodsynopsis
callback(string $filename, string $content): mixed
```

`filename`

Назва файлу.

`content`

Вміст, зчитаний з файлового потоку.

`chunk_size`

Довжина блоку.

`offset`

Зміщення.

### Значення, що повертаються

Чи було читання виконано успішно, чи виникла помилка.
