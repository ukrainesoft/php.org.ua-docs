Отримати список поштових скриньок, імена яких містять заданий рядок

-   [« imap\_listmailbox](function.imap-listmailbox.html)
    
-   [imap\_listsubscribed »](function.imap-listsubscribed.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати список поштових скриньок, імена яких містять заданий рядок
    

# imaplistscan

(PHP 4, PHP 5, PHP 7, PHP 8)

imaplistscan — Отримати список поштових скриньок, імена яких містять заданий рядок

### Опис

```methodsynopsis
imap_listscan(    IMAP\Connection $imap,    string $reference,    string $pattern,    string $content): array|false
```

Повертає масив, що містить імена поштових скриньок, що містять `content` у тексті.

Ця функція схожа на [imap\_listmailbox()](function.imap-listmailbox.html), але також виявляє присутність рядка `content` всередині даних поштової скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`reference`

У `reference`, як правило, повинна бути вказана лише специфікація сервера, як описано в [imap\_open()](function.imap-open.html)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`pattern`

Визначає початок пошуку в ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати при передачі як частину `pattern``*`'і'`%``*`' повертає всі поштові скриньки. Якщо ви передасте `pattern` як '`*`', то отримайте повний список ієрархії поштових скриньок. '`%`' поверне лише поточний рівень. '`%`', переданий як параметр `pattern`, поверне поштові скриньки лише на верхньому рівні; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії ~/mail, крім тих, що знаходяться в її піддиректоріях.

`content`

Шуканий рядок

### Значення, що повертаються

Повертає масив, що містить імена поштових скриньок, що містять `content` у тексті або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_listmailbox()](function.imap-listmailbox.html) - Псевдонім imaplist
-   [imap\_search()](function.imap-search.html) - Отримати повідомлення, які відповідають заданим критеріям