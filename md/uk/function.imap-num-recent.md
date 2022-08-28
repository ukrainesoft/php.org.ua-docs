Отримати кількість нових повідомлень у поточній поштовій скриньці

-   [« imap\_num\_msg](function.imap-num-msg.html)
    
-   [imap\_open »](function.imap-open.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати кількість нових повідомлень у поточній поштовій скриньці
    

# imapnumrecent

(PHP 4, PHP 5, PHP 7, PHP 8)

imapnumrecent — Отримати кількість нових повідомлень у поточній поштовій скриньці

### Опис

```methodsynopsis
imap_num_recent(IMAP\Connection $imap): int
```

Повертає кількість нових повідомлень у поточній поштовій скриньці.

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

### Значення, що повертаються

Повертає кількість нових повідомлень у поточній поштовій скриньці у вигляді цілого числа.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Дивіться також

-   [imap\_num\_msg()](function.imap-num-msg.html) - Отримати кількість повідомлень у поточній поштовій скриньці
-   [imap\_status()](function.imap-status.html) - Отримати інформацію про статус поштової скриньки