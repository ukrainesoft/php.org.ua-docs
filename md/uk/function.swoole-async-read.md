---
navigation:
  - function.swoole-async-dns-lookup.md: « swoole\_async\_dns\_lookup
  - function.swoole-async-readfile.md: swoole\_async\_readfile »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_async\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_async\_read

(PECL swoole >= 1.9.0)

swoole\_async\_read — Асинхронне читання потоку файлу

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
