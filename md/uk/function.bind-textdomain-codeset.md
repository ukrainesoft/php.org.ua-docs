---
navigation:
  - ref.gettext.md: « Функції gettext
  - function.bindtextdomain.md: bindtextdomain »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: bind\_textdomain\_codeset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bind\_textdomain\_codeset

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

bind\_textdomain\_codeset — Встановлює або отримує кодування, де повертатимуться повідомлення з каталогу повідомлень домену

### Опис

```methodsynopsis
bind_textdomain_codeset(string $domain, ?string $codeset): string|false
```

Функция**bind\_textdomain\_codeset()** встановлює або отримує кодування, в якому повертатимуться повідомлення з `domain`, такими функциями как[gettext()](function.gettext.md)

### Список параметрів

`domain`

Домен.

`codeset`

Кодування. Якщо **`null`**, повертається поточне встановлене кодування.

### Значення, що повертаються

Рядок у разі успішного виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.3 | `codeset` тепер допускає значення null. Раніше було неможливо отримати поточне встановлене кодування. |

### Примітки

> **Зауваження** :
> 
> Інформація **bind\_textdomain\_codeset()** зберігається кожному за процесу, а чи не для потоку.
