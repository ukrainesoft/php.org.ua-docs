Отримати заголовки всіх повідомлень у поштовій скриньці

-   [« imapheaderinfo](function.imap-headerinfo.html)
    
-   [imaplasterror »](function.imap-last-error.html)
    
-   [PHP Manual](index.md)
    
-   [Функции IMAP](ref.imap.md)
    
-   Отримати заголовки всіх повідомлень у поштовій скриньці
    

# imapheaders

(PHP 4, PHP 5, PHP 7, PHP 8)

imapheaders — Отримати заголовки всіх повідомлень у поштовій скриньці

### Опис

```methodsynopsis
imap_headers(IMAP\Connection $imap): array|false
```

Повертає заголовки всіх повідомлень у поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAPConnection](class.imap-connection.html)

### Значення, що повертаються

Повертає масив із рядками, що містять заголовки повідомлень. Один елемент – одне повідомлення. Повертає **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAPConnection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |