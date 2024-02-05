---
navigation:
  - function.readline-on-new-line.md: « readline\_on\_new\_line
  - function.readline-redisplay.md: readline\_redisplay »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_read\_history
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_read\_history

(PHP 4, PHP 5, PHP 7, PHP 8)

readline\_read\_history — Прочитати історію команд із файлу

### Опис

```methodsynopsis
readline_read_history(?string $filename = null): bool
```

Функція читає історію команд із файлу.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `filename` тепер допускає значення null. |
