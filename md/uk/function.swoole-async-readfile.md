---
navigation:
  - function.swoole-async-read.md: « swoole\_async\_read
  - function.swoole-async-set.md: swoole\_async\_set »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_async\_readfile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_async\_readfile

(PECL swoole >= 1.9.0)

swoole\_async\_readfile - Асинхронне читання файлу

### Опис

```methodsynopsis
swoole_async_readfile(string $filename, callable $callback): bool
```

### Список параметрів

`filename`

Ім'я файлу для читання.

`callback`

```methodsynopsis
callback(string $filename, string $content): mixed
```

`filename`

Ім'я файлу.

`content`

Вміст з файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
