Видалити поштову скриньку

-   [« imap\_delete](function.imap-delete.html)
    
-   [imap\_errors »](function.imap-errors.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Видалити поштову скриньку
    

# imapdeletemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imapdeletemailbox — Видалити поштову скриньку

### Опис

```methodsynopsis
imap_deletemailbox(IMAP\Connection $imap, string $mailbox): bool
```

Видаляє поштову скриньку `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`mailbox`

Ім'я ящика. Детальніше читайте в описі [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_createmailbox()](function.imap-createmailbox.html) - Створити нову поштову скриньку
-   [imap\_renamemailbox()](function.imap-renamemailbox.html) - Перейменувати поштову скриньку
-   [imap\_open()](function.imap-open.html) - Відкриває потік IMAP до поштової скриньки формату `mbox`