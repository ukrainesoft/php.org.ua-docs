---
navigation:
  - function.imap-renamemailbox.md: « imap\_renamemailbox
  - function.imap-rfc822-parse-adrlist.md: imap\_rfc822\_parse\_adrlist »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_reopen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_reopen

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_reopen — Відкриває потік IMAP до нової скриньки

### Опис

```methodsynopsis
imap_reopen(    IMAP\Connection $imap,    string $mailbox,    int $flags = 0,    int $retries = 0): bool
```

Перевідкриває вказаний потік до скриньки `mailbox` на сервері IMAP чи NNTP.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі про функцію [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

`flags` - бітова маска з однієї або кількох констант:

-   \*\*`OP_READONLY`\*\*- відкрити поштову скриньку лише для читання
-   \*\*`OP_ANONYMOUS`\*\*- не використовувати та не оновлювати .newsrc для новин (тільки NNTP)
-   \*\*`OP_HALFOPEN`\*\*- відкрити з'єднання, але не підключатися до поштової скриньки ім'я IMAP і NNTP.
-   \*\*`OP_EXPUNGE`\*\*- мовчки виконати видалення позначених для видалення повідомлень у потоці
-   \*\*`CL_EXPUNGE`\*\*- автоматично видаляти всі позначені для видалення повідомлення під час закриття поштової скриньки (див.[imap\_delete()](function.imap-delete.md) і [imap\_expunge()](function.imap-expunge.md)) .

`retries`

Максимальна кількість спроб з'єднання

### Значення, що повертаються

Повертає **`true`**, якщо потік перевідкритий і **`false`**, якщо ні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Пример #1 Пример использования**imap\_reopen()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org:143}INBOX", "username", "password") or die(implode(", ", imap_errors()));
// ...
imap_reopen($mbox, "{imap.example.org:143}INBOX.Sent") or die(implode(", ", imap_errors()));
// ..
?>
```
