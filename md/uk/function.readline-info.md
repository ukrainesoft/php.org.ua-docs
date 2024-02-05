---
navigation:
  - function.readline-completion-function.md: « readline\_completion\_function
  - function.readline-list-history.md: readline\_list\_history »
  - index.md: PHP Manual
  - ref.readline.md: Опції Readline
title: readline\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readline\_info

(PHP 4, PHP 5, PHP 7, PHP 8)

readline\_info — Встановлює/читає різні внутрішні змінні readline

### Опис

```methodsynopsis
readline_info(?string $var_name = null, int|string|bool|null $value = null): mixed
```

Встановлює/читає різні внутрішні змінні readline.

### Список параметрів

`var_name`

Ім'я змінної.

`value`

Якщо встановлено, то змінної буде присвоєно це значення.

### Значення, що повертаються

Якщо викликати функцію без параметрів, буде повернуто масив значень всіх внутрішніх змінних readline. У елементів масиву будуть наступні індекси: `done` `end` `erase_empty_line` `library_version` `line_buffer` `mark` `pending_input` `point` `prompt` `readline_name`и`terminal_name`. Масив (array) міститиме лише ті елементи, які підтримуються бібліотекою, яка використовується для складання модуля readline.

Якщо викликати з одним або двома параметрами, то повернеться старе/поточне значення змінної.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `var_name`и`value` тепер допускають значення null. |
