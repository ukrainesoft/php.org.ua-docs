- [« imap_getmailboxes](function.imap-getmailboxes.md)
- [imap_header »](function.imap-header.md)

- [PHP Manual](index.md)
- [Функції IMAP](ref.imap.md)
- Список усіх поштових скриньок, на які ви підписані

#imap_getsubscribed

(PHP 4, PHP 5, PHP 7, PHP 8)

imap_getsubscribed — Список усіх поштових скриньок, на які ви
підписано

### Опис

**imap_getsubscribed**([IMAP\Connection](class.imap-connection.md)
`$imap`, string `$reference`, string `$pattern`): array\|false

Повертає інформацію про список усіх поштових скриньок, на які ви
підписано.

Ідентично [imap_getmailboxes()](function.imap-getmailboxes.md), за
виключенням того, що повертається лише список скриньок, на які
підписано користувачем.

### Список параметрів

`imap`
Примірник [IMAP\Connection](class.imap-connection.md).

`reference`
В `reference`, як правило, має бути вказана лише специфікація
сервера, як описано в [imap_open()](function.imap-open.md)

**Увага**
Якщо
[imap.enable_insecure_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh)
не вимкнено, то передача в цей параметр не перевірених даних *не
безпечна*.

`pattern`
Визначає початок пошуку у ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати під час передачі
як частина `pattern`: '`*`` та '`%''. '`*`' повертає всі поштові скриньки.
Якщо ви передасте `pattern` як ``*``, то отримаєте повний перелік
ієрархії поштових скриньок. ''%'' поверне лише поточний рівень. ''%'',
переданий як параметр `pattern`, поверне поштові скриньки лише на самому
верхній рівень; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії
`~/mail`, крім тих, що знаходяться в її піддиректоріях.

### Значення, що повертаються

Повертає масив об'єктів, що містять інформацію про скриньки. Кожен
об'єкт має властивості: `name`, що містить повне ім'я скриньки; `delimiter`,
містить роздільник для тієї частини ієрархії, в якій міститься
ящик; та `attributes`. Параметр `Attributes` є бітовою маскою,
наступних допустимих констант:

- **`LATT_NOINFERIORS`** - ця скринька не має нащадків (немає жодного
ящика нижче цього).
- **`LATT_NOSELECT`** - це лише контейнер, а не поштова скринька. Ви
не можете відкрити його.
- **`LATT_MARKED`** - Ця скринька позначена. Використовується тільки
UW-IMAPD.
- **`LATT_UNMARKED`** - Ця скринька не помічена. Використовується тільки
UW-IMAPD.
- **`LATT_REFERRAL`** - Цей контейнер має напрямки (referral)
на віддалену поштову скриньку.
- **`LATT_HASCHILDREN`** - Ця поштова скринька має обрані
підлеглі (inferiors).
- **`LATT_HASNOCHILDREN`** - Ця поштова скринька не має обраних
підлеглі (inferiors).

Функція повертає **`false`** у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                                   |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 8.1.0  | Параметр imap тепер чекає на екземпляр [IMAP\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |
