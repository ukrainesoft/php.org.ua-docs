Функція завершення сесії

-   [« session\_regenerate\_id](function.session-regenerate-id.html)
    
-   [session\_reset »](function.session-reset.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Функція завершення сесії
    

# sessionregistershutdown

(PHP 5> = 5.4.0, PHP 7, PHP 8)

sessionregistershutdown - Функція завершення сесії

### Опис

```methodsynopsis
session_register_shutdown(): void
```

Реєструє функцію [session\_write\_close()](function.session-write-close.html) як функція завершення сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

При невдалій реєстрації завершальної функції генерує помилку рівня **`E_WARNING`**