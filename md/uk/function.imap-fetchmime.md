---
navigation:
  - function.imap-fetchheader.html: « imapfetchheader
  - function.imap-fetchstructure.html: imapfetchstructure »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imapfetchmime
---
# imapfetchmime

(PHP 5> = 5.3.6, PHP 7, PHP 8)

imapfetchmime — Вийняти MIME-заголовки для конкретного розділу повідомлення

### Опис

```methodsynopsis
imap_fetchmime(    IMAP\Connection $imap,    int $message_num,    string $section,    int $flags = 0): string|false
```

Витягує MIME-заголовки для конкретного розділу повідомлення.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`message_num`

Номер повідомлення

`section`

Номер розділу повідомлення. Рядок цілих чисел, розділених точками, визначальна частина тіла повідомлення відповідно до специфікації IMAP4

`flags`

Бітова маска з однієї або кількох опцій:

-   **`FT_UID`** - Параметр `message_num` є UID
-   **`FT_PEEK`** - Не встановлювати прапор Seen, якщо його вже не встановлено
-   **`FT_INTERNAL`** - Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.

### Значення, що повертаються

Повертає MIME-заголовки для конкретної секції повідомлення у вигляді рядка або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imapfetchbody()](function.imap-fetchbody.html) - Витягти конкретну секцію тіла повідомлення
-   [imapfetchstructure()](function.imap-fetchstructure.html) - Прочитати структуру вказаного повідомлення
-   [imapfetchheader()](function.imap-fetchheader.html) - Отримати заголовок повідомлення
