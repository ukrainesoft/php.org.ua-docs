---
navigation:
  - function.imap-create.md: « imap\_create
  - function.imap-delete.md: imap\_delete »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_createmailbox
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_createmailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_createmailbox — Створює нову поштову скриньку

### Опис

```methodsynopsis
imap_createmailbox(IMAP\Connection $imap, string $mailbox): bool
```

Створює нову поштову скриньку, вказану в `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`mailbox`

Имя почтового ящика. Более подробно смотрите[imap\_open()](function.imap-open.md). Імена поштових скриньок, що містять міжнародні символи, повинні бути закодовані за допомогою [imap\_utf7\_encode()](function.imap-utf7-encode.md)

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Приклад #1 Приклад використання** imap\_createmailbox()\*\*\*\*

```php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
     or die("не получилось подключиться: " . imap_last_error());

$name1 = "phpnewbox";
$name2 = imap_utf7_encode("phpnewböx"); // phpnewb&w7Y-x

$newname = $name1;

echo "Новым именем будет '$name1'<br />\n";

// теперь создадим новый ящик "phptestbox" в вашем входящем каталоге,
// проверим его статус и удалим, чтобы вернуть ваш каталог к первоначальному
// состоянию

if (@imap_createmailbox($mbox, imap_utf7_encode("{imap.example.org}INBOX.$newname"))) {
    $status = @imap_status($mbox, "{imap.example.org}INBOX.$newname", SA_ALL);
    if ($status) {
        echo "ваш новый почтовый ящик называется '$name1' и имеет следующий статус:<br />\n";
        echo "Сообщений:           " . $status->messages    . "<br />\n";
        echo "Новых:                 " . $status->recent      . "<br />\n";
        echo "Непрочитанных:     " . $status->unseen      . "<br />\n";
        echo "Следующий UID:    " . $status->uidnext     . "<br />\n";
        echo "Корректность UID:" . $status->uidvalidity . "<br />\n";

        if (imap_renamemailbox($mbox, "{imap.example.org}INBOX.$newname", "{imap.example.org}INBOX.$name2")) {
            echo "переименуем новый ящик из '$name1' в '$name2'<br />\n";
            $newname = $name2;
        } else {
            echo "вызов imap_renamemailbox для нового ящика завершился ошибкой: " . imap_last_error() . "<br />\n";
        }
    } else {
        echo "вызов imap_status для нового ящика завершился ошибкой: " . imap_last_error() . "<br />\n";
    }

    if (@imap_deletemailbox($mbox, "{imap.example.org}INBOX.$newname")) {
        echo "новый почтовый ящик удалён для восстановления первоначального состояния<br />\n";
    } else {
        echo "вызов imap_deletemailbox на новом почтовом ящике завершился ошибкой: " . implode("<br />\n", imap_errors()) . "<br />\n";
    }

} else {
    echo "невозможно создать новый почтовый ящик: " . implode("<br />\n", imap_errors()) . "<br />\n";
}

imap_close($mbox);
?>
```

### Дивіться також

-   [imap\_renamemailbox()](function.imap-renamemailbox.md) \- Перейменовує поштову скриньку
-   [imap\_deletemailbox()](function.imap-deletemailbox.md) \- Видаляє поштову скриньку
