Отримати UID за номером повідомлення

-   [« imap\_timeout](function.imap-timeout.html)
    
-   [imap\_undelete »](function.imap-undelete.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Отримати UID за номером повідомлення
    

# imapuid

(PHP 4, PHP 5, PHP 7, PHP 8)

imapuid — Отримати UID за номером повідомлення

### Опис

```methodsynopsis
imap_uid(IMAP\Connection $imap, int $message_num): int|false
```

Ця функція повертає UID для повідомлення із заданим номером. UID - це унікальний ідентифікатор, який не змінюється з часом, у той час як номер повідомлення в скриньці може змінюватися при зміні вмісту поштової скриньки.

Ця функція зворотна функції [imap\_msgno()](function.imap-msgno.html)

### Список параметрів

`imap`

Екземпляр [IMAP\\Connection](class.imap-connection.html)

`message_num`

Номер повідомлення.

### Значення, що повертаються

UID заданого листа.

### список змін

| Версия | Описание                                                                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `imap` тепер чекає екземпляр [IMAP\\Connection](class.imap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Примітки

> **Зауваження**
> 
> Ця функція не підтримується для поштових скриньок POP3.

### Дивіться також

-   [imap\_msgno()](function.imap-msgno.html) - Отримати номер повідомлення із заданим UID