Знімає з повідомлення позначку видалення

-   [« imapuid](function.imap-uid.html)
    
-   [imapunsubscribe »](function.imap-unsubscribe.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Знімає з повідомлення позначку видалення
    

# imapundelete

(PHP 4, PHP 5, PHP 7, PHP 8)

imapundelete — Знімає з повідомлення позначку видалення

### Опис

```methodsynopsis
imap_undelete(IMAP\Connection $imap, string $message_nums, int $flags = 0): bool
```

Видаляє із заданого повідомлення мітку видалення, яка була встановлена ​​за допомогою [imapdelete()](function.imap-delete.html) або [imapmailmove()](function.imap-mail-move.html)

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

`message_nums`

Рядок (string), що складається з одного або декількох повідомлень у форматі послідовності у стилі IMAP4 (`"n"` `"n:m"` або їх комбінація, розділена комами).

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [imapdelete()](function.imap-delete.html) - Позначити повідомлення для видалення
-   [imapmailmove()](function.imap-mail-move.html) - Перемістити вказані повідомлення до вказаної поштової скриньки