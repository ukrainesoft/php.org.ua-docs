Відписатися від поштової скриньки

-   [« imapundelete](function.imap-undelete.html)
    
-   [imaputf7decode »](function.imap-utf7-decode.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Відписатися від поштової скриньки
    

# imapunsubscribe

(PHP 4, PHP 5, PHP 7, PHP 8)

imapunsubscribe — Відписатися від поштової скриньки

### Опис

```methodsynopsis
imap_unsubscribe(IMAP\Connection $imap, string $mailbox): bool
```

Відписатися від поштової скриньки `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки. Детальніше дивіться в розділі про [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapsubscribe()](function.imap-subscribe.html) - Підписатися на поштову скриньку