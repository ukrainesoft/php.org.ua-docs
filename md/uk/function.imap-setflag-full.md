Встановити прапори на повідомлення

-   [« imapsetacl](function.imap-setacl.html)
    
-   [imapsort »](function.imap-sort.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Встановити прапори на повідомлення
    

# imapsetflagfull

(PHP 4, PHP 5, PHP 7, PHP 8)

imapsetflagfull — Встановити прапорці на повідомлення

### Опис

```methodsynopsis
imap_setflag_full(    IMAP\Connection $imap,    string $sequence,    string $flag,    int $options = 0): bool
```

Повідомляє сервер, що треба додати прапор `flag` до набору прапорів, заданих у `sequence` повідомлень.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`sequence`

Послідовність номерів повідомлень. Ви можете перерахувати кілька повідомлень, використовуючи як роздільник кому (`X,Y`), або задати інтервал повідомлень за допомогою двокрапки `X:Y`

`flag`

Прапори, які можна встановити: `\Seen` `\Answered` `\Flagged` `\Deleted` і `\Draft`, як визначено в [» RFC2060](http://www.faqs.org/rfcs/rfc2060)

`options`

Бітова маска, яка може приймати лише одне значення:

-   **`ST_UID`** - Послідовність повідомлень задана не їх номерами, а за допомогою UID

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **imapsetflagfull()****

```php
<?php
$mbox = imap_open("{imap.example.org:143}", "username", "password")
     or die("не удалось подключиться: " . imap_last_error());

$status = imap_setflag_full($mbox, "2,5", "\\Seen \\Flagged");

echo gettype($status) . "\n";
echo $status . "\n";

imap_close($mbox);
?>
```

### Дивіться також

-   [imapclearflagfull()](function.imap-clearflag-full.html) - Зняти з повідомлення встановлені прапори