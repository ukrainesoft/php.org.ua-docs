Копіювати повідомлення до вказаної поштової скриньки

-   [« imapmailcompose](function.imap-mail-compose.html)
    
-   [imapmailmove »](function.imap-mail-move.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Копіювати повідомлення до вказаної поштової скриньки
    

# imapmailcopy

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmailcopy — Скопіювати повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_mail_copy(    IMAP\Connection $imap,    string $message_nums,    string $mailbox,    int $flags = 0): bool
```

Копіює задані в `message_nums` листи у вказану поштову скриньку.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`message_nums`

`message_nums` - це діапазон, а не просто номери повідомлень (як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі, присвяченому функції [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

`flags` - бітова маска однієї або кількох констант:

-   **`CP_UID`** - означає, що у першому параметрі не номери повідомлень, які UID.
-   **`CP_MOVE`** - Видалити оригінальні повідомлення після копіювання. Якщо цей прапор встановлено, функція поводиться ідентично до функції [imapmailmove()](function.imap-mail-move.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapmailmove()](function.imap-mail-move.html) - Перемістити вказані повідомлення у вказану поштову скриньку