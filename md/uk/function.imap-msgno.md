Отримати номер повідомлення із заданим UID

-   [« imap\_mime\_header\_decode](function.imap-mime-header-decode.html)
    
-   [imap\_mutf7\_to\_utf8 »](function.imap-mutf7-to-utf8.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати номер повідомлення із заданим UID
    

# imapmsgno

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmsgno — Отримати номер повідомлення із заданим UID

### Опис

```methodsynopsis
imap_msgno(IMAP\Connection $imap, int $message_uid): int
```

Повертає номер повідомлення для вказаного `message_uid`

Ця функція зворотна до [imap\_uid()](function.imap-uid.html)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`message_uid`

UID повідомлення

### Значення, що повертаються

Повертає номер повідомлення для вказаного `message_uid`

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_uid()](function.imap-uid.html) - Отримати UID за номером повідомлення