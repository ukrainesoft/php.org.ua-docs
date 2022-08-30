Прочитати заголовок повідомлення

-   [« imapheader](function.imap-header.html)
    
-   [imapheaders »](function.imap-headers.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Прочитати заголовок повідомлення
    

# imapheaderinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

imapheaderinfo — Прочитати заголовок повідомлення

### Опис

```methodsynopsis
imap_headerinfo(    IMAP\Connection $imap,    int $message_num,    int $from_length = 0,    int $subject_length = 0): stdClass|false
```

Витягує інформацію про повідомлення з його заголовка.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`message_num`

Номер повідомлення

`from_length`

Кількість символів у властивості `fetchfrom`. Має бути більше або дорівнює нулю.

`subject_length`

Кількість символів у властивості `fetchsubject`. Має бути більше або дорівнює нулю.

`defaulthost`

### Значення, що повертаються

У разі виникнення помилки повертає **`false`**. У разі успішного виконання повертає об'єкт із такими властивостями:

-   toaddress - повний рядок to:, максимум 1024 символів
-   to - масив об'єктів з поля To:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   fromaddress - повний рядок from:, максимум 1024 символів
-   from - масив об'єктів з поля From:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   ccaddress - повний рядок cc: максимум 1024 символів
-   cc - масив об'єктів з поля Cc:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   bccaddress - повний рядок bcc:, максимум 1024 символів
-   bcc - масив об'єктів з поля Bcc:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   replytoaddress - повний рядок Reply-To:, максимум 1024 символів
-   replyto - масив об'єктів з поля Reply-To:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   senderaddress - повний рядок sender:, максимум 1024 символів
-   sender - масив об'єктів з поля Sender:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   returnpathaddress - повний рядок Return-Path:, максимум 1024 символів
-   returnpath - масив об'єктів з поля Return-Path:, з наступними властивостями: `personal` `adl` `mailbox` і `host`
-   remail -
-   date - Дата листа, як вона вказана в заголовку
-   Date - Те саме, що і date
-   subject - Тема листа
-   Subject - Те саме, що й subject
-   інreplyto -
-   messageid -
-   newsgroups -
-   followupto -
-   references -
-   Recent - `R` якщо нове та прочитане, `N` якщо нове і не прочитане, якщо не нове.
-   Unseen - `U` якщо НЕ прочитано і НЕ нове, ' ' якщо прочитано АБО не прочитано і нове
-   Flagged - `F` якщо зазначено, ' ' якщо ні
-   Answered - `A` якщо повідомлено, ' ' якщо ні
-   Deleted - `D` якщо видалено, ' ' якщо ні
-   Draft - `X` якщо чернетка, ' ' якщо ні
-   Msgno - Номер повідомлення
-   MailDate -
-   Size - Розмір повідомлення
-   udate - час відсилання у вигляді тимчасової мітки Unix
-   fetchfrom - поле from, відформатоване відповідно до `from_length`
-   fetchsubject - поле subject, відформатоване відповідно до `subject_length`

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|        | Параметр, що не використовується `defaulthost` був видалений.                                                                                        |

### Дивіться також

-   [imapfetchoverview()](function.imap-fetch-overview.html) - Огляд інформації, що міститься в заголовках повідомлень