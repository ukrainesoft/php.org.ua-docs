---
navigation:
  - function.dcgettext.md: « dcgettext
  - function.dgettext.md: dgettext »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: dcngettext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dcngettext

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

dcngettext — Версія dcgettext для множини

### Опис

```methodsynopsis
dcngettext(    string $domain,    string $singular,    string $plural,    int $count,    int $category): string
```

Ця функція дозволяє перевизначити одне повідомлення з використанням множини в поточному домені.

### Список параметрів

`domain`

Домен.

`singular`

`plural`

`count`

`category`

### Значення, що повертаються

У разі успішного виконання повертає рядок (string).

### Дивіться також

-   [ngettext()](function.ngettext.md) \- Версія gettext для повідомлень у множині
