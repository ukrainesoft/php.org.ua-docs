Вийняти MIME-заголовки для конкретного розділу повідомлення

-   [« imap\_fetchheader](function.imap-fetchheader.html)
    
-   [imap\_fetchstructure »](function.imap-fetchstructure.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Вийняти MIME-заголовки для конкретного розділу повідомлення
    

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

Екземпляр [IMAP\\Connection](class.imap-connection.html)

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

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_fetchbody()](function.imap-fetchbody.html) - Витягти конкретну секцію тіла повідомлення
-   [imap\_fetchstructure()](function.imap-fetchstructure.html) - Прочитати структуру вказаного повідомлення
-   [imap\_fetchheader()](function.imap-fetchheader.html) - Отримати заголовок повідомлення