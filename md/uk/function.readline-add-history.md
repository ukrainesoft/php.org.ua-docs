---
navigation:
  - ref.readline.md: « Функції Readline
  - function.readline-callback-handler-install.md: readline\_callback\_handler\_install »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_add\_history
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_add\_history

(PHP 4, PHP 5, PHP 7, PHP 8)

readline\_add\_history — Додає рядок до історії

### Опис

```methodsynopsis
readline_add_history(string $prompt): bool
```

Додає рядок до історії введення.

### Список параметрів

`prompt`

Рядок, який треба додати в історію команд.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
