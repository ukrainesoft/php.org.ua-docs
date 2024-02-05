---
navigation:
  - function.dcngettext.md: « dcngettext
  - function.dngettext.md: dngettext »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: dgettext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dgettext

(PHP 4, PHP 5, PHP 7, PHP 8)

dgettext — Перевизначення поточного домену для одного повідомлення

### Опис

```methodsynopsis
dgettext(string $domain, string $message): string
```

Функция**dgettext()** дозволяє перевизначити поточний домен `domain` для одного повідомлення.

### Список параметрів

`domain`

Домен.

`message`

Повідомлення.

### Значення, що повертаються

У разі успішного виконання, повертає значення типу string.

### Дивіться також

-   [gettext()](function.gettext.md) \- Шукає повідомлення у поточному домені
