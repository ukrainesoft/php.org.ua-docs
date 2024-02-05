---
navigation:
  - function.imap-fetchbody.md: « imap\_fetchbody
  - function.imap-fetchmime.md: imap\_fetchmime »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_fetchheader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_fetchheader

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_fetchheader — Отримує заголовок повідомлення

### Опис

```methodsynopsis
imap_fetchheader(IMAP\Connection $imap, int $message_num, int $flags = 0): string|false
```

Ця функція отримує повний, нефільтрований заголовок у форматі [» RFC2822](http://www.faqs.org/rfcs/rfc2822) для заданого повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_num`

Номер повідомлення

`flags`

Допустимі значення `flags` :

-   \*\*`FT_UID`\*\*- Параметр`message_num`є UID
-   \*\*`FT_INTERNAL`\*\*- Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.
-   **`FT_PREFETCHTEXT`** - одночасно має бути підвантажений RFC822.TEXT. Це дозволяє уникнути зайвого RTT при з'єднанні IMAP, якщо вибрано повний текст повідомлення (наприклад, під час операції "зберегти у файл")

### Значення, що повертаються

Повертає заголовок повідомлення у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_fetch\_overview()](function.imap-fetch-overview.md) \- Оглядає інформацію із заголовків повідомлень
