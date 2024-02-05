---
navigation:
  - function.imap-mail.md: « imap\_mail
  - function.imap-mime-header-decode.md: imap\_mime\_header\_decode »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_mailboxmsginfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_mailboxmsginfo

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_mailboxmsginfo — Отримує інформацію про поточну поштову скриньку

### Опис

```methodsynopsis
imap_mailboxmsginfo(IMAP\Connection $imap): stdClass
```

Перевірка статусу поточної поштової скриньки на сервері. Аналогічно [imap\_status()](function.imap-status.md), але додатково обчислює сумарний розмір всіх листів у ящику, через що працює дещо повільніше.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

### Значення, що повертаються

Повертає об'єкт із наступними полями:

< td>ім'я поштової скриньки

<table class="doctable table"><caption><strong>Властивості поштової скриньки</strong></caption><tbody class="tbody"><tr><td>Date</td><td>дата останньої зміни (поточна дата та час)</td></tr><tr><td>Driver</td><td>драйвер</td></tr><tr><td>Mailbox</td></tr><tr><td>Nmsgs</td><td>кількість листів</td></tr><tr><td>Recent</td><td>кількість нових</td></tr><tr><td>Unread</td><td>кількість непрочитаних</td></tr><tr><td>Deleted</td><td>кількість віддалених</td></tr><tr><td>Size</td><td>розмір скриньки</td></tr></tbody></table>

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |

### Приклади

**Пример #1 Пример использования**imap\_mailboxmsginfo()\*\*\*\*

```php
<?php

$mbox = imap_open("{imap.example.org}INBOX", "username", "password")
      or die("не удалось подключиться: " . imap_last_error());

$check = imap_mailboxmsginfo($mbox);

if ($check) {
    echo "Date: "     . $check->Date    . "<br />\n" ;
    echo "Driver: "   . $check->Driver  . "<br />\n" ;
    echo "Mailbox: "  . $check->Mailbox . "<br />\n" ;
    echo "Messages: " . $check->Nmsgs   . "<br />\n" ;
    echo "Recent: "   . $check->Recent  . "<br />\n" ;
    echo "Unread: "   . $check->Unread  . "<br />\n" ;
    echo "Deleted: "  . $check->Deleted . "<br />\n" ;
    echo "Size: "     . $check->Size    . "<br />\n" ;
} else {
    echo "Вызов imap_mailboxmsginfo() завершился с ошибкой: " . imap_last_error() . "<br />\n";
}

imap_close($mbox);

?>
```
