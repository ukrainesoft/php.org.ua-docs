---
navigation:
  - function.imap-header.md: « imap\_header
  - function.imap-headers.md: imap\_headers »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_headerinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_headerinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_headerinfo — Читає заголовок повідомлення

### Опис

```methodsynopsis
imap_headerinfo(    IMAP\Connection $imap,    int $message_num,    int $from_length = 0,    int $subject_length = 0): stdClass|false
```

Витягує інформацію про повідомлення з його заголовка.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

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
-   to - масив об'єктів з поля To:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   fromaddress - повний рядок from:, максимум 1024 символів
-   from - масив об'єктів з поля From:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   ccaddress - повний рядок cc: максимум 1024 символів
-   cc - масив об'єктів з поля Cc:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   bccaddress - повний рядок bcc:, максимум 1024 символів
-   bcc - масив об'єктів з поля Bcc:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   reply\_toaddress - повний рядок Reply-To:, максимум 1024 символів
-   reply\_to - масив об'єктів з поля Reply-To:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   senderaddress - повний рядок sender:, максимум 1024 символів
-   sender - масив об'єктів з поля Sender:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   return\_pathaddress - повний рядок Return-Path:, максимум 1024 символів
-   return\_path - масив об'єктів з поля Return-Path:, з наступними властивостями:`personal` `adl` `mailbox`и`host`
-   remail -
-   date - Дата листа, як вона вказана в заголовку
-   Date - Те саме, що і date
-   subject - Тема листа
-   Subject - Те саме, що і subject
-   in\_reply\_to -
-   message\_id -
-   newsgroups -
-   followup\_to -
-   references -
-   Recent -`R`якщо нове та прочитане,`N` якщо нове і не прочитане, якщо не нове.
-   Unseen -`U` якщо НЕ прочитано і НЕ нове, ' ' якщо прочитано АБО не прочитано і нове
-   Flagged -`F` якщо зазначено, ' ' якщо ні
-   Answered -`A` якщо повідомлено, ' ' якщо ні
-   Deleted -`D` якщо видалено, ' ' якщо ні
-   Draft -`X` якщо чернетка, ' ' якщо ні
-   Msgno - Номер повідомлення
-   MailDate -
-   Size - Розмір повідомлення
-   udate - час відсилання у вигляді тимчасової мітки Unix
-   fetchfrom - поле from, відформатоване відповідно до`from_length`
-   fetchsubject - поле subject, відформатоване відповідно до`subject_length`

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | Параметр, що не використовується`defaulthost`був видалений. |

### Дивіться також

-   [imap\_fetch\_overview()](function.imap-fetch-overview.md) \- Оглядає інформацію із заголовків повідомлень
