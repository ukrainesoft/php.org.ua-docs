---
navigation:
  - function.imap-binary.md: « imap\_binary
  - function.imap-bodystruct.md: imap\_bodystruct »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_body
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_body

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_body — Читає тіло повідомлення

### Опис

```methodsynopsis
imap_body(IMAP\Connection $imap, int $message_num, int $flags = 0): string|false
```

**imap\_body()** повертає тіло повідомлення з номером `message_num` у поточній поштовій скриньці.

**imap\_body()** поверне точну копію тіла повідомлення. Для отримання однієї частини складеного MIME-повідомлення використовуйте [imap\_fetchstructure()](function.imap-fetchstructure.md) для аналізу структури та [imap\_fetchbody()](function.imap-fetchbody.md) для отримання копії однієї з частин тіла.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_num`

Номер повідомлення

`flags`

Опціональний параметр `flags`, що є бітовою маскою однієї або декількох констант:

-   **`FT_UID`** `message_num`є UID
-   \*\*`FT_PEEK`\*\*- Не встановлювати прапор Переглянуто (\\Seen), якщо його вже не встановлено.
-   \*\*`FT_INTERNAL`\*\*- рядок, що повертається, буде у внутрішньому форматі, а не канонізований до CRLF.

### Значення, що повертаються

Повертає рядок із тілом зазначеного повідомлення або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
