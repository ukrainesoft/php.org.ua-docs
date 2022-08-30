Перейменувати поштову скриньку

-   [« imaprename](function.imap-rename.html)
    
-   [imapreopen »](function.imap-reopen.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Перейменувати поштову скриньку
    

# imaprenamemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imaprenamemailbox — Перейменувати поштову скриньку

### Опис

```methodsynopsis
imap_renamemailbox(IMAP\Connection $imap, string $from, string $to): bool
```

Ця функція перейменовує oldmbox у newmbox (формат імені `mbox` дивіться в описі [imapopen()](function.imap-open.html)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`from`

Старе ім'я. Детальніше читайте в описі [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`to`

Нове ім'я Детальніше читайте в описі [imapopen()](function.imap-open.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapcreatemailbox()](function.imap-createmailbox.html) - Створити нову поштову скриньку
-   [imapdeletemailbox()](function.imap-deletemailbox.html) - Видалити поштову скриньку