---
navigation:
  - function.imap-fetch-overview.md: « imap\_fetch\_overview
  - function.imap-fetchheader.md: imap\_fetchheader »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_fetchbody
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_fetchbody

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_fetchbody — Витягує конкретну секцію тіла повідомлення

### Опис

```methodsynopsis
imap_fetchbody(    IMAP\Connection $imap,    int $message_num,    string $section,    int $flags = 0): string|false
```

Витягує конкретну секцію тіла повідомлення. Секції повідомлення у цій функції не декодуються.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_num`

Номер повідомлення

`section`

Номер розділу повідомлення. Рядок цілих чисел, розділених точками, визначальна частина тіла повідомлення відповідно до специфікації IMAP4

`flags`

Бітова маска з однієї або кількох опцій:

-   \*\*`FT_UID`\*\*- Параметр`message_num`є UID
-   \*\*`FT_PEEK`\*\*- Не встановлювати прапор\\Seen, якщо він уже не встановлений
-   \*\*`FT_INTERNAL`\*\*- Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.

### Значення, що повертаються

Повертає конкретну секцію тіла повідомлення у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_savebody()](function.imap-savebody.md) \- Зберігає частину тіла повідомлення у файл
-   [imap\_fetchstructure()](function.imap-fetchstructure.md) \- Читає структуру вказаного повідомлення
