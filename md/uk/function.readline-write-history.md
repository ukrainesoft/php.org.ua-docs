---
navigation:
  - function.readline-redisplay.md: « readlineredisplay
  - function.readline.md: readline »
  - index.md: PHP Manual
  - ref.readline.md: Функции Readline
title: readlinewritehistory
---
# readlinewritehistory

(PHP 4, PHP 5, PHP 7, PHP 8)

readlinewritehistory — Записати історію команд у файл

### Опис

```methodsynopsis
readline_write_history(?string $filename = null): bool
```

Функція записує історію команд у файл.

### Список параметрів

`filename`

Шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `filename` тепер допускає значення null. |
