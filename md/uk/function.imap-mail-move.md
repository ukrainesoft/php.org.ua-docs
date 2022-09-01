---
navigation:
  - function.imap-mail-copy.html: « imapmailcopy
  - function.imap-mail.html: imapmail »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imapmailmove
---
# imapmailmove

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmailmove — Перемістити вказані повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_mail_move(    IMAP\Connection $imap,    string $message_nums,    string $mailbox,    int $flags = 0): bool
```

Переміщує листи, задані в `message_nums` у вказану поштову скриньку `mailbox`. Зверніть увагу, що поштові повідомлення фактично *копіюються* в `mailbox`, а вихідні повідомлення позначаються для видалення. Це означає, що повідомлення в `mailbox` призначаються нові UID.

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

`flags` - бітова маска, яка може приймати лише одне значення:

-   **`CP_UID`** - означає, що в першому параметрі не номери повідомлень, а їх UID

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Примітки

> **Зауваження**
> 
> Функція **imapmailmove()** позначає оригінальне повідомлення прапором видалення, тому не забудьте після неї викликати функцію [imapexpunge()](function.imap-expunge.html)

### Дивіться також

-   [imapmailcopy()](function.imap-mail-copy.html) - Скопіювати повідомлення у вказану поштову скриньку
