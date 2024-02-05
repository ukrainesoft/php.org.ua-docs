---
navigation:
  - function.imap-alerts.md: « imap\_alerts
  - function.imap-base64.md: imap\_base64 »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_append
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_append

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_append — Додає рядкове повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_append(    IMAP\Connection $imap,    string $folder,    string $message,    ?string $options = null,    ?string $internal_date = null): bool
```

Додає рядок `message` у вказаний `folder`

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.md)

`folder`

Имя почтового ящика. Смотрите[imap\_open()](function.imap-open.md) для детальної інформації.

**Увага**

Якщо [imap.enable\_insecure\_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`message`

Повідомлення, що додається у вигляді рядка

При зверненні до сервера Cyrus IMAP слід використовувати "\\r\\n" як завершальний символ рядка замість "\\n", інакше операція буде невдалою.

`options`

Если указан, то параметр`options`также будет записан в`folder`

`internal_date`

Якщо цей параметр вказано, він встановить INTERNALDATE у повідомленні, що додається. Параметр повинен містити дату, подану рядком, що відповідає специфікації rfc2060 для значення date\_time.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `imap` |
| 8.0.0 | `options`и`internal_date` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання** imap\_append()\*\*\*\*

```php
<?php
$imap = imap_open("{imap.example.org}INBOX.Drafts", "username", "password");

$check = imap_check($imap);
echo "Кол-во сообщений до добавления: ". $check->Nmsgs . "\n";

imap_append($imap, "{imap.example.org}INBOX.Drafts"
                   , "From: me@example.com\r\n"
                   . "To: you@example.com\r\n"
                   . "Subject: test\r\n"
                   . "\r\n"
                   . "это проверочное сообщение, пожалуйста, игнорируйте его\r\n"
                   );

$check = imap_check($imap);
echo "Кол-во сообщений после добавления : ". $check->Nmsgs . "\n";

imap_close($imap);
?>
```
