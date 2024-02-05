---
navigation:
  - function.imap-createmailbox.md: « imap\_createmailbox
  - function.imap-deletemailbox.md: imap\_deletemailbox »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_delete

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_delete — Позначає повідомлення для видалення

### Опис

```methodsynopsis
imap_delete(IMAP\Connection $imap, string $message_nums, int $flags = 0): true
```

Позначає повідомлення, перелічені у `message_nums` для видалення. Позначені повідомлення залишатимуться в скриньці доки не буде викликана функція [imap\_expunge()](function.imap-expunge.md), либо[imap\_close()](function.imap-close.md) із встановленим параметром **`CL_EXPUNGE`**

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`message_nums`

Рядок (string), що складається з одного або декількох повідомлень у форматі послідовності у стилі IMAP4 (`"n"` `"n:m"` або їх комбінація, розділена комами).

`flags`

Можна поставити як \*\*`FT_UID`\*\*тоді функція буде очікувати в параметрі `message_nums` не номер повідомлення, а `UID`

### Значення, що повертаються

Функція завжди повертає **`true`**

### Помилки

Викидає виняток [ValueError](class.valueerror.md), если значение параметра`flags`недопустимо.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | Тепер викидається виняток[ValueError](class.valueerror.md), при неприпустимих значеннях параметра `flags`. . Раніше виникало попередження та функція повертала логічне значення **`false`** |

### Приклади

**Приклад #1 Приклад використання** imap\_delete()\*\*\*\*

```php
<?php

$mbox = imap_open("{imap.example.org}INBOX", "username", "password")
    or die("Не удалось подключиться: " . imap_last_error());

$check = imap_mailboxmsginfo($mbox);
echo "Сообщения до отметки для удаления: " . $check->Nmsgs . "<br />\n";

imap_delete($mbox, 1);

$check = imap_mailboxmsginfo($mbox);
echo "Сообщения после отметки для удаления: " . $check->Nmsgs . "<br />\n";

imap_expunge($mbox);

$check = imap_mailboxmsginfo($mbox);
echo "Сообщения после удаления: " . $check->Nmsgs . "<br />\n";

imap_close($mbox);
?>
```

### Примітки

> **Зауваження** :
> 
> Скриньки IMAP можуть не зберігати прапори між з'єднаннями, отже якщо ви дійсно хочете видалити позначені повідомлення, необхідно викликати [imap\_expunge()](function.imap-expunge.md) у тому ж з'єднанні, в якому встановлювалися прапори.

### Дивіться також

-   [imap\_undelete()](function.imap-undelete.md) \- Знімає з повідомлення позначку видалення
-   [imap\_expunge()](function.imap-expunge.md) \- Видаляє всі позначені для видалення повідомлення
-   [imap\_close()](function.imap-close.md) \- Закриває потік IMAP
