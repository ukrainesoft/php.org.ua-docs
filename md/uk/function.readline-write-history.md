---
navigation:
  - function.readline-redisplay.md: « readline\_redisplay
  - function.readline.md: readline »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_write\_history
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_write\_history

(PHP 4, PHP 5, PHP 7, PHP 8)

readline\_write\_history — Записати історію команд у файл

### Опис

```methodsynopsis
readline_write_history(?string $filename = null): bool
```

Функція записує історію команд у файл.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `filename` тепер допускає значення null. |
