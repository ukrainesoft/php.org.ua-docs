---
navigation:
  - function.imap-getmailboxes.md: « imap\_getmailboxes
  - function.imap-header.md: imap\_header »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_getsubscribed
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_getsubscribed

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_getsubscribed — Отримує список усіх поштових скриньок, на які оформлена передплата

### Опис

```methodsynopsis
imap_getsubscribed(IMAP\Connection $imap, string $reference, string $pattern): array|false
```

Повертає інформацію про список усіх поштових скриньок, на які ви підписані.

Ідентично [imap\_getmailboxes()](function.imap-getmailboxes.md), за винятком того, що повертається лише список скриньок, на які підписано користувач.

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

### Значення, що повертаються

Повертає масив об'єктів, що містять інформацію про скриньки. Кожен об'єкт має властивості: `name`, содержащее полное имя ящика;`delimiter`містить роздільник для тієї частини ієрархії, в якій міститься ящик; і `attributes`Параметр`Attributes` є бітовою маскою, наступних допустимих констант:

-   \*\*`LATT_NOINFERIORS`\*\*- цей ящик немає нащадків (немає жодного ящика нижче цього).
-   \*\*`LATT_NOSELECT`\*\*- це лише контейнер, а не поштова скринька. Ви не можете його відкрити.
-   \*\*`LATT_MARKED`\*\*- Ця скринька помічена. Використовується лише UW-IMAPD.
-   \*\*`LATT_UNMARKED`\*\*- Ця скринька не помічена. Використовується лише UW-IMAPD.
-   \*\*`LATT_REFERRAL`\*\*- Цей контейнер має напрямки (referral) на віддалену поштову скриньку.
-   \*\*`LATT_HASCHILDREN`\*\*- Ця поштова скринька має підпорядковані (inferiors).
-   \*\*`LATT_HASNOCHILDREN`\*\*- Ця поштова скринька не має підлеглі (inferiors).

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
