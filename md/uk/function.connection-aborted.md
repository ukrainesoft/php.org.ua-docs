Перевірити, чи клієнт вимкнено

-   [« Різні функції](ref.misc.md)
    
-   [connectionstatus »](function.connection-status.html)
    
-   [PHP Manual](index.md)
    
-   [Різні функції](ref.misc.md)
    
-   Перевірити, чи клієнт вимкнено
    

# connectionaborted

(PHP 4, PHP 5, PHP 7, PHP 8)

connectionaborted — Перевірити, чи клієнт вимкнено

### Опис

```methodsynopsis
connection_aborted(): int
```

Перевіряє, чи клієнт вимкнено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 1, якщо клієнт вимкнено, 0 інакше.

### Дивіться також

-   [connectionstatus()](function.connection-status.html) - Повертає статус з'єднання у бітах
-   [ignoreuserabort()](function.ignore-user-abort.html) - Встановити, чи має відключення клієнта переривати виконання скрипту
-   Дивіться [Управление подключениями](features.connection-handling.html) для отримання повного опису управління підключення PHP.