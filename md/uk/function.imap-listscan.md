---
navigation:
  - function.imap-listmailbox.md: « imap\_listmailbox
  - function.imap-listsubscribed.md: imap\_listsubscribed »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_listscan
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_listscan

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_listscan — Отримує список поштових скриньок, імена яких містять заданий рядок

### Опис

```methodsynopsis
imap_listscan(    IMAP\Connection $imap,    string $reference,    string $pattern,    string $content): array|false
```

Повертає масив, що містить імена поштових скриньок, що містять `content`в тексте.

Ця функція схожа на [imap\_listmailbox()](function.imap-listmailbox.md), але також виявляє присутність рядка `content` всередині даних поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`reference`

В`reference`, як правило, повинна бути вказана лише специфікація сервера, як описано в [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`pattern`

Визначає початок пошуку в ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати при передачі як частину `pattern`: '`*`'і'`%`'. '`*`' повертає всі поштові скриньки. Якщо ви передасте `pattern` як '`*`', то отримайте повний список ієрархії поштових скриньок. '`%`' поверне лише поточний рівень. '`%`', переданий як параметр `pattern`, поверне поштові скриньки лише на верхньому рівні; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії ~/mail, крім тих, що знаходяться в її піддиректорії.

`content`

Шуканий рядок

### Значення, що повертаються

Повертає масив, що містить імена поштових скриньок, що містять `content`в тексте или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_listmailbox()](function.imap-listmailbox.md) \- Псевдонім imap\_list
-   [imap\_search()](function.imap-search.md) \- Отримує повідомлення, які відповідають заданим критеріям
