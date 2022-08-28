Підписатися на поштову скриньку

-   [« imap\_status](function.imap-status.html)
    
-   [imap\_thread »](function.imap-thread.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Підписатися на поштову скриньку
    

# imapsubscribe

(PHP 4, PHP 5, PHP 7, PHP 8)

imapsubscribe — Передплатити поштову скриньку

### Опис

```methodsynopsis
imap_subscribe(IMAP\Connection $imap, string $mailbox): bool
```

Передплатити нову поштову скриньку.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки. Детальніше читай у розділі про [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_unsubscribe()](function.imap-unsubscribe.html) - Відписатися від поштової скриньки