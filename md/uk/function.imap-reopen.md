Перевідкриває потік IMAP до нової скриньки

-   [« imap\_renamemailbox](function.imap-renamemailbox.html)
    
-   [imap\_rfc822\_parse\_adrlist »](function.imap-rfc822-parse-adrlist.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Перевідкриває потік IMAP до нової скриньки
    

# imapreopen

(PHP 4, PHP 5, PHP 7, PHP 8)

imapreopen — Відкриває потік IMAP до нової скриньки

### Опис

```methodsynopsis
imap_reopen(    IMAP\Connection $imap,    string $mailbox,    int $flags = 0,    int $retries = 0): bool
```

Перевідкриває вказаний потік до скриньки `mailbox` на сервері IMAP чи NNTP.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки. Докладніше читайте у розділі про функцію [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

`flags` - бітова маска з однієї або кількох констант:

-   **`OP_READONLY`** - відкрити поштову скриньку лише для читання
-   **`OP_ANONYMOUS`** - не використовувати та не оновлювати .newsrc для новин (тільки NNTP)
-   **`OP_HALFOPEN`** - відкрити з'єднання, але не підключатися до поштової скриньки для IMAP і NNTP.
-   **`OP_EXPUNGE`** - мовчки виконати видалення позначених для видалення повідомлень у потоці
-   **`CL_EXPUNGE`** - автоматично видаляти всі позначені для видалення повідомлення під час закриття поштової скриньки (див. [imap\_delete()](function.imap-delete.html) і [imap\_expunge()](function.imap-expunge.html)

`retries`

Максимальна кількість спроб з'єднання

### Значення, що повертаються

Повертає **`true`**, якщо потік перевідкритий і **`false`**, якщо ні.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imapreopen()****

```php
<?php
$mbox = imap_open("{imap.example.org:143}INBOX", "username", "password") or die(implode(", ", imap_errors()));
// ...
imap_reopen($mbox, "{imap.example.org:143}INBOX.Sent") or die(implode(", ", imap_errors()));
// ..
?>
```