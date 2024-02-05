---
navigation:
  - function.swoole-async-set.md: « swoole\_async\_set
  - function.swoole-async-writefile.md: swoole\_async\_writefile »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_async\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_async\_write

(PECL swoole >= 1.9.0)

swoole\_async\_write — Асинхронний запис даних до потоку файлу

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
