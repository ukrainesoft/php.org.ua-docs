Прочитати список поштових скриньок

-   [« imap\_last\_error](function.imap-last-error.html)
    
-   [imap\_listmailbox »](function.imap-listmailbox.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Прочитати список поштових скриньок
    

# imaplist

(PHP 4, PHP 5, PHP 7, PHP 8)

imaplist — Прочитати список поштових скриньок

### Опис

```methodsynopsis
imap_list(IMAP\Connection $imap, string $reference, string $pattern): array|false
```

Читає список поштових скриньок.

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

### Значення, що повертаються

Повертає масив з іменами поштових скриньок або **`false`** у разі невдачі.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imaplist()****

```php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$list = imap_list($mbox, "{imap.example.org}", "*");
if (is_array($list)) {
    foreach ($list as $val) {
        echo imap_utf7_decode($val) . "\n";
    }
} else {
    echo "вызов imap_list завершился с ошибкой: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```

### Дивіться також

-   [imap\_getmailboxes()](function.imap-getmailboxes.html) - Прочитати список поштових скриньок, повертаючи докладну інформацію щодо кожного з них
-   [imap\_lsub()](function.imap-lsub.html) - Список усіх підписаних поштових скриньок