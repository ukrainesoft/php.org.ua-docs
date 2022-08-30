Отримати інформацію про поточну поштову скриньку

-   [« imapmail](function.imap-mail.html)
    
-   [imapmimeheaderdecode »](function.imap-mime-header-decode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати інформацію про поточну поштову скриньку
    

# imapmailboxmsginfo

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmailboxmsginfo — Отримати інформацію про поточну поштову скриньку

### Опис

```methodsynopsis
imap_mailboxmsginfo(IMAP\Connection $imap): stdClass
```

Перевірка статусу поточної поштової скриньки на сервері. Аналогічно [imapstatus()](function.imap-status.html), але додатково обчислює сумарний розмір всіх листів у ящику, через що працює дещо повільніше.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

### Значення, що повертаються

Повертає об'єкт із наступними полями:

< td>ім'я поштової скриньки

<table class="doctable table"><caption><strong>Властивості поштової скриньки</strong></caption><tbody class="tbody"><tr><td>Date</td><td>дата останньої зміни (поточна дата та час)</td></tr><tr><td>Driver</td><td>драйвер</td></tr><tr><td>Mailbox</td></tr><tr><td>Nmsgs</td><td>кількість листів</td></tr><tr><td>Recent</td><td>кількість нових</td></tr><tr><td>Unread</td><td>кількість непрочитаних</td></tr><tr><td>Deleted</td><td>кількість віддалених</td></tr><tr><td>Size</td><td>розмір скриньки</td></tr></tbody></table>

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Описание                                                                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imapmailboxmsginfo()****

```php
<?php

$mbox = imap_open("{imap.example.org}INBOX", "username", "password")
      or die("не удалось подключиться: " . imap_last_error());

$check = imap_mailboxmsginfo($mbox);

if ($check) {
    echo "Date: "     . $check->Date    . "<br />\n" ;
    echo "Driver: "   . $check->Driver  . "<br />\n" ;
    echo "Mailbox: "  . $check->Mailbox . "<br />\n" ;
    echo "Messages: " . $check->Nmsgs   . "<br />\n" ;
    echo "Recent: "   . $check->Recent  . "<br />\n" ;
    echo "Unread: "   . $check->Unread  . "<br />\n" ;
    echo "Deleted: "  . $check->Deleted . "<br />\n" ;
    echo "Size: "     . $check->Size    . "<br />\n" ;
} else {
    echo "Вызов imap_mailboxmsginfo() завершился с ошибкой: " . imap_last_error() . "<br />\n";
}

imap_close($mbox);

?>
```