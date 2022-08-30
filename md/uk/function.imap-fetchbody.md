Витягти конкретну секцію тіла повідомлення

-   [« imapfetchoverview](function.imap-fetch-overview.html)
    
-   [imapfetchheader »](function.imap-fetchheader.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Витягти конкретну секцію тіла повідомлення
    

# imapfetchbody

(PHP 4, PHP 5, PHP 7, PHP 8)

imapfetchbody — Витягти конкретну секцію тіла повідомлення

### Опис

```methodsynopsis
imap_fetchbody(    IMAP\Connection $imap,    int $message_num,    string $section,    int $flags = 0): string|false
```

Витягує конкретну секцію тіла повідомлення. Секції повідомлення у цій функції не декодуються.

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

Повертає конкретну секцію тіла повідомлення у вигляді рядка або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imapsavebody()](function.imap-savebody.html) - Зберегти частину тіла повідомлення у файл
-   [imapfetchstructure()](function.imap-fetchstructure.html) - Прочитати структуру вказаного повідомлення