Відписатися від поштової скриньки

-   [« imap\_undelete](function.imap-undelete.html)
    
-   [imap\_utf7\_decode »](function.imap-utf7-decode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
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

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки. Детальніше дивіться в розділі про [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_subscribe()](function.imap-subscribe.html) - Підписатися на поштову скриньку