---
navigation:
  - function.bindtextdomain.md: « bindtextdomain
  - function.dcngettext.md: dcngettext »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: dcgettext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dcgettext

(PHP 4, PHP 5, PHP 7, PHP 8)

dcgettext — Перевизначення одного повідомлення в домені

### Опис

```methodsynopsis
dcgettext(string $domain, string $message, int $category): string
```

Ця функція дозволяє перевизначити поточний домен для одного повідомлення.

### Список параметрів

`domain`

Домен

`message`

Повідомлення

`category`

Категорія

### Значення, що повертаються

У разі успішного виконання, повертає значення типу string.

### Дивіться також

-   [gettext()](function.gettext.md) \- Шукає повідомлення у поточному домені
