---
navigation:
  - function.swoole-async-write.md: « swoole\_async\_write
  - function.swoole-clear-error.md: swoole\_clear\_error »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_async\_writefile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_async\_writefile

(PECL swoole >= 1.9.0)

swoole\_async\_writefile — Асинхронний запис даних у файл

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
