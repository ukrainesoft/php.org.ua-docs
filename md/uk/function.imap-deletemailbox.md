---
navigation:
  - function.imap-delete.md: « imap\_delete
  - function.imap-errors.md: imap\_errors »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_deletemailbox
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_deletemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_deletemailbox — Видаляє поштову скриньку

### Опис

```methodsynopsis
imap_deletemailbox(IMAP\Connection $imap, string $mailbox): bool
```

Видаляє поштову скриньку `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Ім'я ящика. Детальніше читайте в описі [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_createmailbox()](function.imap-createmailbox.md) \- Створює нову поштову скриньку
-   [imap\_renamemailbox()](function.imap-renamemailbox.md) \- Перейменовує поштову скриньку
-   [imap\_open()](function.imap-open.md) \- Відкриває потік IMAP до поштової скриньки формату`mbox`
