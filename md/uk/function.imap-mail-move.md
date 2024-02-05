---
navigation:
  - function.imap-mail-copy.md: « imap\_mail\_copy
  - function.imap-mail.md: imap\_mail »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_mail\_move
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_mail\_move

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_mail\_move — Переміщує вказані повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_mail_move(    IMAP\Connection $imap,    string $message_nums,    string $mailbox,    int $flags = 0): bool
```

Переміщує листи, задані у параметрі `message_nums` у вказаний у параметрі `mailbox` Поштова скринька. Зверніть увагу, що поштові повідомлення фактично *копіюються* у ящик `mailbox`, а вихідні повідомлення позначаються для видалення. Це означає, що повідомлення в ящиках `mailbox` призначаються нові UID.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_nums`

`message_nums` - це діапазон, а не просто номери повідомлень (як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі, присвяченому функції [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

`flags` - бітова маска, яка може приймати лише одне значення:

-   \*\*`CP_UID`\*\*- означає, що в першому параметрі не номери повідомлень, а їх UID

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Примітки

> **Зауваження** :
> 
> Функция**imap\_mail\_move()** позначає оригінальне повідомлення прапором видалення, тому не забудьте після неї викликати функцію [imap\_expunge()](function.imap-expunge.md)

### Дивіться також

-   [imap\_mail\_copy()](function.imap-mail-copy.md) \- Копіює повідомлення у вказану поштову скриньку
