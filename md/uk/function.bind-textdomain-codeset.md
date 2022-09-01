---
navigation:
  - ref.gettext.html: « Функции gettext
  - function.bindtextdomain.html: bindtextdomain »
  - index.html: PHP Manual
  - ref.gettext.html: Функции gettext
title: bindtextdomaincodeset
---
# bindtextdomaincodeset

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

bindtextdomaincodeset — Встановлює або отримує кодування, де повертатимуться повідомлення з каталогу повідомлень домену

### Опис

```methodsynopsis
bind_textdomain_codeset(string $domain, ?string $codeset): string|false
```

Функція **bindtextdomaincodeset()** встановлює або отримує кодування, в якому повертатимуться повідомлення з `domain`, такими функціями як [gettext()](function.gettext.html)

### Список параметрів

`domain`

Домен.

`codeset`

Кодування. Якщо **`null`**, повертається поточне встановлене кодування.

### Значення, що повертаються

Рядок у разі успішного виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `codeset` тепер допускає значення null. Раніше було неможливо отримати поточне встановлене кодування. |

### Примітки

> **Зауваження**
> 
> Інформація **bindtextdomaincodeset()** зберігається кожному за процесу, а чи не для потоку.
