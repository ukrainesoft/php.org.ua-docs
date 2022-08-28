Видалити всі позначені для видалення повідомлення

-   [« imap\_errors](function.imap-errors.html)
    
-   [imap\_fetch\_overview »](function.imap-fetch-overview.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Видалити всі позначені для видалення повідомлення
    

# imapexpunge

(PHP 4, PHP 5, PHP 7, PHP 8)

imapexpunge — Видалити всі позначені для видалення повідомлення

### Опис

```methodsynopsis
imap_expunge(IMAP\Connection $imap): bool
```

Видаляє всі позначені для видалення повідомлення. Позначити для видалення можна за допомогою функцій [imap\_delete()](function.imap-delete.html) [imap\_mail\_move()](function.imap-mail-move.html) або [imap\_setflag\_full()](function.imap-setflag-full.html)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

### Значення, що повертаються

Повертає **`true`**

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |