---
navigation:
  - function.imap-rename.md: « imap\_rename
  - function.imap-reopen.md: imap\_reopen »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_renamemailbox
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_renamemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_renamemailbox — Перейменовує поштову скриньку

### Опис

```methodsynopsis
imap_renamemailbox(IMAP\Connection $imap, string $from, string $to): bool
```

Ця функція перейменовує old\_mbox у new\_mbox (формат имени параметра`mbox`дан в описании функции[imap\_open()](function.imap-open.md)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`from`

Старое имя. Более подробно читайте в описании[imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`to`

Нове ім'я Детальніше читайте в описі [imap\_open()](function.imap-open.md)

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
-   [imap\_deletemailbox()](function.imap-deletemailbox.md) \- Видаляє поштову скриньку
