Позначити повідомлення для видалення

-   [« imap\_createmailbox](function.imap-createmailbox.html)
    
-   [imap\_deletemailbox »](function.imap-deletemailbox.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Позначити повідомлення для видалення
    

# imapdelete

(PHP 4, PHP 5, PHP 7, PHP 8)

imapdelete — Позначити повідомлення для видалення

### Опис

```methodsynopsis
imap_delete(IMAP\Connection $imap, string $message_nums, int $flags = 0): bool
```

Позначає повідомлення, перелічені у `message_nums` для видалення. Позначені повідомлення залишатимуться в скриньці доки не буде викликана функція [imap\_expunge()](function.imap-expunge.html), або [imap\_close()](function.imap-close.html) із встановленим параметром **`CL_EXPUNGE`**

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`message_nums`

Рядок (string), що складається з одного або декількох повідомлень у форматі послідовності у стилі IMAP4 (`"n"` `"n:m"` або їх комбінація, розділена комами).

`flags`

Можна поставити як **`FT_UID`**тоді функція буде очікувати в параметрі `message_nums` не номер повідомлення, а `UID`

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **imapdelete()****

```php
<?php

$mbox = imap_open("{imap.example.org}INBOX", "username", "password")
    or die("Не удалось подключиться: " . imap_last_error());

$check = imap_mailboxmsginfo($mbox);
echo "Сообщения до отметки для удаления: " . $check->Nmsgs . "<br />\n";

imap_delete($mbox, 1);

$check = imap_mailboxmsginfo($mbox);
echo "Сообщения после отметки для удаления: " . $check->Nmsgs . "<br />\n";

imap_expunge($mbox);

$check = imap_mailboxmsginfo($mbox);
echo "Сообщения после удаления: " . $check->Nmsgs . "<br />\n";

imap_close($mbox);
?>
```

### Примітки

> **Зауваження**
> 
> Скриньки IMAP можуть не зберігати прапори між з'єднаннями, тому якщо ви дійсно хочете видалити позначені повідомлення, необхідно викликати [imap\_expunge()](function.imap-expunge.html) у тому з'єднанні, в якому прапори встановлювалися.

### Дивіться також

-   [imap\_undelete()](function.imap-undelete.html) - Знімає з повідомлення позначку видалення
-   [imap\_expunge()](function.imap-expunge.html) - Видалити всі позначені для видалення повідомлення
-   [imap\_close()](function.imap-close.html) - Закрити потік IMAP