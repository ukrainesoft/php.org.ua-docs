---
navigation:
  - function.imap-getacl.md: « imap\_getacl
  - function.imap-getsubscribed.md: imap\_getsubscribed »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_getmailboxes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_getmailboxes

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_getmailboxes — Читає список поштових скриньок, повертаючи докладну інформацію щодо кожної з них

### Опис

```methodsynopsis
imap_getmailboxes(IMAP\Connection $imap, string $reference, string $pattern): array|false
```

Отримує інформацію про поштові скриньки.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`reference`

`reference` зазвичай має бути лише специфікацією сервера, як описано в [imap\_open()](function.imap-open.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`pattern`

Визначає початок пошуку в ієрархії поштових скриньок.

Є два спеціальні символи, які можна використовувати при передачі як частину `pattern`: '`*`'і'`%`'. '`*`' повертає всі поштові скриньки. Якщо ви передасте `pattern` як '`*`', то отримайте повний список ієрархії поштових скриньок. '`%`' поверне лише поточний рівень. '`%`', переданий як параметр `pattern`, поверне поштові скриньки лише на верхньому рівні; '`~/mail/%`' на `UW_IMAPD` поверне всі ящики в директорії ~/mail, крім тих, що знаходяться в її піддиректорії.

### Значення, що повертаються

Повертає масив об'єктів, що містять інформацію про скриньки. Кожен об'єкт має властивості: `name`, содержащее полное имя ящика;`delimiter`містить роздільник для тієї частини ієрархії, в якій міститься ящик; і `attributes`Параметр`Attributes` є бітовою маскою, наступних допустимих констант:

-   \*\*`LATT_NOINFERIORS`\*\*- цей ящик немає і може мати нащадків (утримувати вкладені ящики). Виклик функції[imap\_createmailbox()](function.imap-createmailbox.md)не працюватиме для цієї скриньки.
    
-   \*\*`LATT_NOSELECT`\*\*- це лише контейнер, а не поштова скринька. Ви не можете його відкрити.
    
-   \*\*`LATT_MARKED`\*\*- Ця скринька помічена. Це означає, що в ньому можуть бути нові листи, що з'явилися з моменту останньої перевірки. Не працює з усіма серверами IMAP.
    
-   \*\*`LATT_UNMARKED`**\- Ця скринька не помічена, тобто. у ньому немає нових листів. Якщо один із прапорів**`MARKED`** або **`UNMARKED`\*\*виставлений - вважаєте, що сервер підтримує цей функціонал.
    
-   \*\*`LATT_REFERRAL`\*\*- Цей контейнер має напрямки (referral) на віддалену поштову скриньку.
    
-   \*\*`LATT_HASCHILDREN`\*\*- Ця поштова скринька має підпорядковані (inferiors).
    
-   \*\*`LATT_HASNOCHILDREN`\*\*- Ця поштова скринька не має підлеглі (inferiors).
    

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_getmailboxes()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$list = imap_getmailboxes($mbox, "{imap.example.org}", "*");
if (is_array($list)) {
    foreach ($list as $key => $val) {
        echo "($key) ";
        echo imap_utf7_decode($val->name) . ",";
        echo "'" . $val->delimiter . "',";
        echo $val->attributes . "<br />\n";
    }
} else {
    echo "вызов imap_getmailboxes завершился с ошибкой: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```

### Дивіться також

-   [imap\_getsubscribed()](function.imap-getsubscribed.md) \- Отримує список усіх поштових скриньок, на які оформлена передплата
