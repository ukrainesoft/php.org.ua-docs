---
navigation:
  - function.swoole-async-set.md: « swooleasyncset
  - function.swoole-async-writefile.md: swooleasyncwritefile »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функции Swoole
title: swooleasyncwrite
---
# swooleasyncwrite

(PECL swoole >= 1.9.0)

swooleasyncwrite — Асинхронний запис даних до потоку файлу

### Опис

```methodsynopsis
swoole_async_write(    string $filename,    string $content,    int $offset = ?,    callable $callback = ?): bool
```

### Список параметрів

`filename`

Ім'я файлу, в який буде зроблено запис

`content`

Вміст, що записується у файл.

`offset`

Зміщення.

`callback`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
