---
navigation:
  - function.readline-on-new-line.html: « readlineвінnewline
  - function.readline-redisplay.html: readlineredisplay »
  - index.md: PHP Manual
  - ref.readline.md: Функции Readline
title: readlinereadhistory
---
# readlinereadhistory

(PHP 4, PHP 5, PHP 7, PHP 8)

readlinereadhistory — Прочитати історію команд із файлу

### Опис

```methodsynopsis
readline_read_history(?string $filename = null): bool
```

Функція читає історію команд із файлу.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `filename` тепер допускає значення null. |
