---
navigation:
  - function.imap-fetchheader.md: « imap\_fetchheader
  - function.imap-fetchstructure.md: imap\_fetchstructure »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_fetchmime
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_fetchmime

(PHP 5 >= 5.3.6, PHP 7, PHP 8)

imap\_fetchmime — Витягує MIME-заголовки для конкретної секції повідомлення

### Опис

```methodsynopsis
imap_fetchmime(    IMAP\Connection $imap,    int $message_num,    string $section,    int $flags = 0): string|false
```

Витягує MIME-заголовки для конкретного розділу повідомлення.

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

Повертає MIME-заголовки для конкретної секції повідомлення у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Дивіться також

-   [imap\_fetchbody()](function.imap-fetchbody.md) \- Витягує конкретну секцію тіла повідомлення
-   [imap\_fetchstructure()](function.imap-fetchstructure.md) \- Читає структуру вказаного повідомлення
-   [imap\_fetchheader()](function.imap-fetchheader.md) \- Отримує заголовок повідомлення
