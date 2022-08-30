Додає рядкове повідомлення до вказаної поштової скриньки

-   [« imapalerts](function.imap-alerts.html)
    
-   [imapbase64 »](function.imap-base64.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Додає рядкове повідомлення до вказаної поштової скриньки
    

# imapappend

(PHP 4, PHP 5, PHP 7, PHP 8)

imapappend — Додає рядкове повідомлення до вказаної поштової скриньки

### Опис

```methodsynopsis
imap_append(    IMAP\Connection $imap,    string $folder,    string $message,    ?string $options = null,    ?string $internal_date = null): bool
```

Додає рядок `message` у вказаний `folder`

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`folder`

Ім'я поштової скриньки. Дивіться [imapopen()](function.imap-open.html) для детальної інформації.

**Увага**

Якщо [imap.enableinsecurersh](imap.configuration.html#ini.imap.enable-insecure-rsh) не вимкнено, то передача в цей параметр не перевірених даних *не безпечна*

`message`

Повідомлення, що додається у вигляді рядка

При зверненні до сервера Cyrus IMAP слід використовувати "рn" як завершальний символ рядка замість "n", інакше операція буде невдалою.

`options`

Якщо вказано, то параметр `options` також буде записано в `folder`

`internal_date`

Якщо цей параметр вказано, він встановить INTERNALDATE у повідомленні, що додається. Параметр повинен містити дату, подану рядком, що відповідає специфікації rfc2060 для значення datetime.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | `options` і `internal_date` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **imapappend()****

```php
<?php
$imap = imap_open("{imap.example.org}INBOX.Drafts", "username", "password");

$check = imap_check($imap);
echo "Кол-во сообщений до добавления: ". $check->Nmsgs . "\n";

imap_append($imap, "{imap.example.org}INBOX.Drafts"
                   , "From: me@example.com\r\n"
                   . "To: you@example.com\r\n"
                   . "Subject: test\r\n"
                   . "\r\n"
                   . "это проверочное сообщение, пожалуйста, игнорируйте его\r\n"
                   );

$check = imap_check($imap);
echo "Кол-во сообщений после добавления : ". $check->Nmsgs . "\n";

imap_close($imap);
?>
```