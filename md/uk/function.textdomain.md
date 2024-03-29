---
navigation:
  - function.ngettext.md: « ngettext
  - book.iconv.md: iconv »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: textdomain
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# textdomain

(PHP 4, PHP 5, PHP 7, PHP 8)

textdomain — Встановлює домен за промовчанням

### Опис

```methodsynopsis
textdomain(?string $domain): string
```

Ця функція встановлює домен, у якому буде здійснюватися пошук під час виклику функції [gettext()](function.gettext.md)зазвичай називається ім'ям програми.

### Список параметрів

`domain`

Новий домен повідомлень, або **`null`** для отримання поточного значення без зміни.

### Значення, що повертаються

У разі успішного виконання функція повертає поточний домен повідомлень після можливої ​​його зміни.

### Примітки

> **Зауваження** :
> 
> Інформація **textdomain()** зберігається кожному за процесу, а чи не для потоку.
