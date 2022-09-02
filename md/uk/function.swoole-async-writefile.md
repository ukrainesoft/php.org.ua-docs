---
navigation:
  - function.swoole-async-write.md: « swooleasyncwrite
  - function.swoole-clear-error.md: swooleclearerror »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функции Swoole
title: swooleasyncwritefile
---
# swooleasyncwritefile

(PECL swoole >= 1.9.0)

swooleasyncwritefile — Асинхронний запис даних у файл

### Опис

```methodsynopsis
swoole_async_writefile(    string $filename,    string $content,    callable $callback = ?,    int $flags = 0): bool
```

### Список параметрів

`filename`

Ім'я файлу, в який буде зроблено запис.

`content`

Вміст, що записується у файл.

`callback`

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
