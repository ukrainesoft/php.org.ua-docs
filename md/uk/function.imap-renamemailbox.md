---
navigation:
  - function.imap-rename.md: « imaprename
  - function.imap-reopen.md: imapreopen »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imaprenamemailbox
---
# imaprenamemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imaprenamemailbox — Перейменувати поштову скриньку

### Опис

```methodsynopsis
imap_renamemailbox(IMAP\Connection $imap, string $from, string $to): bool
```

Ця функція перейменовує oldmbox у newmbox (формат імені `mbox` дивіться в описі [imapopen()](function.imap-open.md)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`from`

Старе ім'я. Детальніше читайте в описі [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`to`

Нове ім'я Детальніше читайте в описі [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapcreatemailbox()](function.imap-createmailbox.md) - Створити нову поштову скриньку
-   [imapdeletemailbox()](function.imap-deletemailbox.md) - Видалити поштову скриньку
