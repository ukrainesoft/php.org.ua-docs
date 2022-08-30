Функція завершення сесії

-   [« sessionregenerateід](function.session-regenerate-id.html)
    
-   [sessionreset »](function.session-reset.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи із сесіями](ref.session.html)
    
-   Функція завершення сесії
    

# sessionregistershutdown

(PHP 5> = 5.4.0, PHP 7, PHP 8)

sessionregistershutdown - Функція завершення сесії

### Опис

```methodsynopsis
session_register_shutdown(): void
```

Реєструє функцію [sessionwriteclose()](function.session-write-close.html) як функція завершення сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

При невдалій реєстрації завершальної функції генерує помилку рівня **`E_WARNING`**