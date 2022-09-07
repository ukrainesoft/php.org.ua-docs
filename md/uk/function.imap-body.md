---
navigation:
  - function.imap-binary.md: « imapbinary
  - function.imap-bodystruct.md: imapbodystruct »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapbody
---
# imapbody

(PHP 4, PHP 5, PHP 7, PHP 8)

imapbody — Прочитати тіло повідомлення

### Опис

```methodsynopsis
imap_body(IMAP\Connection $imap, int $message_num, int $flags = 0): string|false
```

**imapbody()** повертає тіло повідомлення з номером `message_num` у поточній поштовій скриньці.

**imapbody()** поверне точну копію тіла повідомлення. Для отримання однієї частини складеного MIME-повідомлення використовуйте [imapfetchstructure()](function.imap-fetchstructure.md) для аналізу структури та [imapfetchbody()](function.imap-fetchbody.md) для отримання копії однієї з частин тіла.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`message_num`

Номер повідомлення

`flags`

Опціональний параметр `flags`, що є бітовою маскою однієї або декількох констант:

-   **`FT_UID`** `message_num` є UID
-   **`FT_PEEK`** - Не встановлювати прапор Переглянуто (Seen), якщо його вже не встановлено.
-   **`FT_INTERNAL`** - рядок, що повертається, буде у внутрішньому форматі, а не канонізований до CRLF.

### Значення, що повертаються

Повертає рядок із тілом зазначеного повідомлення або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
