---
navigation:
  - function.imap-create.html: « imapcreate
  - function.imap-delete.html: imapdelete »
  - index.html: PHP Manual
  - ref.imap.html: Функции IMAP
title: imapcreatemailbox
---
# imapcreatemailbox

(PHP 4, PHP 5, PHP 7, PHP 8)

imapcreatemailbox — Створити нову поштову скриньку

### Опис

```methodsynopsis
imap_createmailbox(IMAP\Connection $imap, string $mailbox): bool
```

Створює нову поштову скриньку, вказану в `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`mailbox`

Ім'я поштової скриньки. Детальніше дивіться [imapopen()](function.imap-open.html). Імена поштових скриньок, що містять міжнародні символи, повинні бути закодовані за допомогою [imaputf7encode()](function.imap-utf7-encode.html)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imapcreatemailbox()****

```php
<?php
$mbox = imap_open("{imap.example.org}", "username", "password", OP_HALFOPEN)
     or die("не получилось подключиться: " . imap_last_error());

$name1 = "phpnewbox";
$name2 = imap_utf7_encode("phpnewböx"); // phpnewb&w7Y-x

$newname = $name1;

echo "Новым именем будет '$name1'<br />\n";

// теперь создадим новый ящик "phptestbox" в вашем входящем каталоге,
// проверим его статус и удалим, чтобы вернуть ваш каталог к первоначальному
// состоянию

if (@imap_createmailbox($mbox, imap_utf7_encode("{imap.example.org}INBOX.$newname"))) {
    $status = @imap_status($mbox, "{imap.example.org}INBOX.$newname", SA_ALL);
    if ($status) {
        echo "ваш новый почтовый ящик называется '$name1' и имеет следующий статус:<br />\n";
        echo "Сообщений:           " . $status->messages    . "<br />\n";
        echo "Новых:                 " . $status->recent      . "<br />\n";
        echo "Непрочитанных:     " . $status->unseen      . "<br />\n";
        echo "Следующий UID:    " . $status->uidnext     . "<br />\n";
        echo "Корректность UID:" . $status->uidvalidity . "<br />\n";

        if (imap_renamemailbox($mbox, "{imap.example.org}INBOX.$newname", "{imap.example.org}INBOX.$name2")) {
            echo "переименуем новый ящик из '$name1' в '$name2'<br />\n";
            $newname = $name2;
        } else {
            echo "вызов imap_renamemailbox для нового ящика завершился ошибкой: " . imap_last_error() . "<br />\n";
        }
    } else {
        echo "вызов imap_status для нового ящика завершился ошибкой: " . imap_last_error() . "<br />\n";
    }

    if (@imap_deletemailbox($mbox, "{imap.example.org}INBOX.$newname")) {
        echo "новый почтовый ящик удалён для восстановления первоначального состояния<br />\n";
    } else {
        echo "вызов imap_deletemailbox на новом почтовом ящике завершился ошибкой: " . implode("<br />\n", imap_errors()) . "<br />\n";
    }

} else {
    echo "невозможно создать новый почтовый ящик: " . implode("<br />\n", imap_errors()) . "<br />\n";
}

imap_close($mbox);
?>
```

### Дивіться також

-   [imaprenamemailbox()](function.imap-renamemailbox.html) - Перейменувати поштову скриньку
-   [imapdeletemailbox()](function.imap-deletemailbox.html) - Видалити поштову скриньку
