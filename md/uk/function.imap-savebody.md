Зберегти частину тіла повідомлення у файл

-   [« imap\_rfc822\_write\_address](function.imap-rfc822-write-address.html)
    
-   [imap\_scan »](function.imap-scan.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Зберегти частину тіла повідомлення у файл
    

# imapsavebody

(PHP 5> = 5.1.3, PHP 7, PHP 8)

imapsavebody — Зберегти частину тіла повідомлення у файл

### Опис

```methodsynopsis
imap_savebody(    IMAP\Connection $imap,    resource|string|int $file,    int $message_num,    string $section = "",    int $flags = 0): bool
```

Записує частину тіла повідомлення у файл.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`file`

Шлях до файлу у вигляді рядка або відкритий за допомогою [fopen()](function.fopen.html) файловий дескриптор.

`message_num`

Номер повідомлення

`section`

Номер розділу повідомлення. Рядок цілих чисел, розділених точками, визначальна частина тіла повідомлення відповідно до специфікації IMAP4

`flags`

Бітова маска з однієї або кількох опцій:

-   **`FT_UID`** - The `message_num` is a UID
-   **`FT_PEEK`** - Не встановлювати прапор Seen, якщо його вже не встановлено
-   **`FT_INTERNAL`** - Повертати рядок у внутрішньому форматі, без перетворення кінців рядків до CRLF.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_fetchbody()](function.imap-fetchbody.html) - Витягти конкретну секцію тіла повідомлення