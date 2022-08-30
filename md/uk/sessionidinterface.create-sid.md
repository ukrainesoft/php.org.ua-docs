Створити ідентифікатор сесії

-   [« SessionIdInterface](class.sessionidinterface.html)
    
-   [SessionUpdateTimestampHandlerInterface »](class.sessionupdatetimestamphandlerinterface.html)
    
-   [PHP Manual](index.html)
    
-   [SessionIdInterface](class.sessionidinterface.html)
    
-   Створити ідентифікатор сесії
    

# SessionIdInterface::createsid

(PHP 5> = 5.5.1, PHP 7, PHP 8)

SessionIdInterface::createsid — Створити ідентифікатор сесії

### Опис

```methodsynopsis
public SessionIdInterface::create_sid(): string
```

Створює новий ідентифікатор сесії. Функція автоматично виконується, коли потрібно створити новий ідентифікатор сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Новий ідентифікатор сесії Зауважте, що це значення повертається всередині PHP для обробки.

### Дивіться також

-   [SessionHandler::createsid()](sessionhandler.create-sid.html) - Повертає новий ідентифікатор сесії