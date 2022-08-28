Отримати заголовки всіх повідомлень у поштовій скриньці

-   [« imap\_headerinfo](function.imap-headerinfo.html)
    
-   [imap\_last\_error »](function.imap-last-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
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

Екземпляр [IMAP\\Connection](class.imap-connection.html)

### Значення, що повертаються

Повертає масив із рядками, що містять заголовки повідомлень. Один елемент – одне повідомлення. Повертає **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |