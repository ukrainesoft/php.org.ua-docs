---
navigation:
  - function.imap-sort.md: « imapsort
  - function.imap-subscribe.md: imapsubscribe »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapstatus
---
# imapstatus

(PHP 4, PHP 5, PHP 7, PHP 8)

imapstatus — Отримати інформацію про статус поштової скриньки

### Опис

```methodsynopsis
imap_status(IMAP\Connection $imap, string $mailbox, int $flags): stdClass|false
```

Повертає інформацію щодо статусу заданої скриньки `mailbox`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.md)

`mailbox`

Ім'я поштової скриньки, докладніше дивіться в описі [imapopen()](function.imap-open.md)

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`flags`

Допустимі опції:

-   **`SA_MESSAGES`** - встановити $status->messages, рівним кількості листів у ящику
-   **`SA_RECENT`** - встановити $status->recent, рівним кількості нових листів
-   **`SA_UNSEEN`** - встановити $status->unseen, рівним кількості непрочитаних листів
-   **`SA_UIDNEXT`** - встановити $status->uidnext рівним наступному uid, який буде використаний у ящику
-   **`SA_UIDVALIDITY`** - встановити $status->uidvalidity у значення константи, яка змінюється, коли UID для поштової скриньки більше не можуть бути дійсними
-   **`SA_ALL`** - Використовувати всі перелічені опції

### Значення, що повертаються

Функція повертає об'єкт, що містить інформацію про статус або **`false`** у разі виникнення помилки. Об'єкт має такі властивості: `messages` `recent` `unseen` `uidnext` і `uidvalidity`

`flags` також встановлено, він містить бітову маску, яка може бути перевірена за допомогою перерахованих вище констант.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapstatus()****

```php
<?php
$mbox = imap_open("{imap.example.com}", "username", "password", OP_HALFOPEN)
      or die("не удалось подключиться: " . imap_last_error());

$status = imap_status($mbox, "{imap.example.org}INBOX", SA_ALL);
if ($status) {
  echo "Сообщения:   " . $status->messages    . "<br />\n";
  echo "Последние:     " . $status->recent      . "<br />\n";
  echo "Непросмотренные:     " . $status->unseen      . "<br />\n";
  echo "UIDnext:    " . $status->uidnext     . "<br />\n";
  echo "UIDvalidity:" . $status->uidvalidity . "<br />\n";
} else {
  echo "imap_status failed: " . imap_last_error() . "\n";
}

imap_close($mbox);
?>
```
