---
navigation:
  - function.imap-fetchbody.md: « imapfetchbody
  - function.imap-fetchmime.md: imapfetchmime »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapfetchheader
---
# imapfetchheader

(PHP 4, PHP 5, PHP 7, PHP 8)

imapfetchheader — Отримати назву повідомлення

### Опис

```methodsynopsis
imap_fetchheader(IMAP\Connection $imap, int $message_num, int $flags = 0): string|false
```

Ця функція отримує повний, нефільтрований заголовок у форматі [» RFC2822](http://www.faqs.org/rfcs/rfc2822) для заданого повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`message_num`

Номер повідомлення

`flags`

Допустимі значення `flags`

-   **`FT_UID`** - Параметр `message_num` є UID
-   **`FT_INTERNAL`** - Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.
-   **`FT_PREFETCHTEXT`** - одночасно має бути підвантажений RFC822.TEXT. Це дозволяє уникнути зайвого RTT при з'єднанні IMAP, якщо вибрано повний текст повідомлення (наприклад, під час операції "зберегти у файл")

### Значення, що повертаються

Повертає заголовок повідомлення у вигляді рядка або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapfetchoverview()](function.imap-fetch-overview.md) - Огляд інформації, що міститься в заголовках повідомлень
