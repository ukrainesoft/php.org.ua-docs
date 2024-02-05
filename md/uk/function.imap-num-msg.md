---
navigation:
  - function.imap-mutf7-to-utf8.md: « imap\_mutf7\_to\_utf8
  - function.imap-num-recent.md: imap\_num\_recent »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_num\_msg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_num\_msg

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_num\_msg — Отримує кількість повідомлень у поточній поштовій скриньці

### Опис

```methodsynopsis
imap_num_msg(IMAP\Connection $imap): int|false
```

Повертає кількість повідомлень у поточній поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає кількість повідомлень у поточній поштовій скриньці у вигляді цілого числа. У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_num\_recent()](function.imap-num-recent.md) \- Отримує кількість нових повідомлень у поточній поштовій скриньці
-   [imap\_status()](function.imap-status.md) \- Отримує інформацію щодо статусу поштової скриньки
