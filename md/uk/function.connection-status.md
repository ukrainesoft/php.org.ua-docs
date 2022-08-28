Повертає статус з'єднання у бітах

-   [« connection\_aborted](function.connection-aborted.html)
    
-   [constant »](function.constant.html)
    
-   [PHP Manual](index.html)
    
-   [Разные функции](ref.misc.html)
    
-   Повертає статус з'єднання у бітах
    

# connectionstatus

(PHP 4, PHP 5, PHP 7, PHP 8)

connectionstatus — Повертає статус з'єднання в бітах

### Опис

```methodsynopsis
connection_status(): int
```

Набуває статусу з'єднання в бітах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає статус з'єднання в бітах, який можна використовувати у константах `CONNECTION_XXX` визначення статусу з'єднання.

### Дивіться також

-   [connection\_aborted()](function.connection-aborted.html) - Перевірити, чи клієнт вимкнено
-   [ignore\_user\_abort()](function.ignore-user-abort.html) - Встановити, чи має відключення клієнта переривати виконання скрипту
-   Дивіться [Управление соединением](features.connection-handling.html) для повної інформації про управління з'єднанням PHP.