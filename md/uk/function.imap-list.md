---
navigation:
  - function.imap-last-error.md: « imap\_last\_error
  - function.imap-listmailbox.md: imap\_listmailbox »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_list
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_list

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_list — Читає список поштових скриньок

### Опис

```methodsynopsis
imap_list(IMAP\Connection $imap, string $reference, string $pattern): array|false
```

Читає список поштових скриньок.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`reference`

В`reference`, як правило, повинна бути вказана лише специфікація сервера, як описано в [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`pattern`

Визначає початок пошуку в ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати при передачі як частину `pattern`: '`*`'і'`%`'. '`*`' повертає всі поштові скриньки. Якщо ви передасте `pattern` як '`*`', то отримайте повний список ієрархії поштових скриньок. '`%`' поверне лише поточний рівень. '`%`', переданий як параметр `pattern`, поверне поштові скриньки лише на верхньому рівні; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії ~/mail, крім тих, що знаходяться в її піддиректорії.

### Значення, що повертаються

Повертає масив з іменами поштових скриньок або \*\*`false`\*\*в случае неудачи.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Пример #1 Пример использования**imap\_list()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$list = imap_list($mbox, "{imap.example.org}", "*");
if (is_array($list)) {
    foreach ($list as $val) {
        echo imap_utf7_decode($val) . "\n";
    }
} else {
    echo "вызов imap_list завершился с ошибкой: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```

### Дивіться також

-   [imap\_getmailboxes()](function.imap-getmailboxes.md) \- Читає список поштових скриньок, повертаючи докладну інформацію щодо кожного з них
-   [imap\_lsub()](function.imap-lsub.md) \- Отримує список усіх поштових скриньок, на які оформлена передплата
