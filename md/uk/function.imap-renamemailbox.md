Перейменувати поштову скриньку

-   [« imap\_rename](function.imap-rename.html)
    
-   [imap\_reopen »](function.imap-reopen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Перейменувати поштову скриньку
    

# imaprenamemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imaprenamemailbox — Перейменувати поштову скриньку

### Опис

```methodsynopsis
imap_renamemailbox(IMAP\Connection $imap, string $from, string $to): bool
```

Ця функція перейменовує oldmbox у newmbox (формат імені `mbox` дивіться в описі [imap\_open()](function.imap-open.html)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`from`

Старе ім'я. Детальніше читайте в описі [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`to`

Нове ім'я Детальніше читайте в описі [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_createmailbox()](function.imap-createmailbox.html) - Створити нову поштову скриньку
-   [imap\_deletemailbox()](function.imap-deletemailbox.html) - Видалити поштову скриньку