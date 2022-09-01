---
navigation:
  - ref.readline.md: « Функции Readline
  - function.readline-callback-handler-install.html: readlinecallbackhandlerinstall »
  - index.md: PHP Manual
  - ref.readline.md: Функции Readline
title: readlineaddhistory
---
# readlineaddhistory

(PHP 4, PHP 5, PHP 7, PHP 8)

readlineaddhistory — Додає рядок до історії

### Опис

```methodsynopsis
readline_add_history(string $prompt): bool
```

Додає рядок до історії введення.

### Список параметрів

`prompt`

Рядок, який треба додати в історію команд.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
