Знімає з повідомлення позначку видалення

-   [« imap\_uid](function.imap-uid.html)
    
-   [imap\_unsubscribe »](function.imap-unsubscribe.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Знімає з повідомлення позначку видалення
    

# imapundelete

(PHP 4, PHP 5, PHP 7, PHP 8)

imapundelete — Знімає з повідомлення позначку видалення

### Опис

```methodsynopsis
imap_undelete(IMAP\Connection $imap, string $message_nums, int $flags = 0): bool
```

Видаляє із заданого повідомлення мітку видалення, яка була встановлена ​​за допомогою [imap\_delete()](function.imap-delete.html) або [imap\_mail\_move()](function.imap-mail-move.html)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`message_nums`

Рядок (string), що складається з одного або декількох повідомлень у форматі послідовності у стилі IMAP4 (`"n"` `"n:m"` або їх комбінація, розділена комами).

`flags`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_delete()](function.imap-delete.html) - Позначити повідомлення для видалення
-   [imap\_mail\_move()](function.imap-mail-move.html) - Перемістити вказані повідомлення до вказаної поштової скриньки