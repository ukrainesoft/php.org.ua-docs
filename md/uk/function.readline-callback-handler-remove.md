Видаляє раніше зареєстровану callback-функцію та відновлює термінал

-   [« readlinecallbackhandlerinstall](function.readline-callback-handler-install.html)
    
-   [readlinecallbackreadchar »](function.readline-callback-read-char.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Readline](ref.readline.html)
    
-   Видаляє раніше зареєстровану callback-функцію та відновлює термінал
    

# readlinecallbackhandlerremove

(PHP 5> = 5.1.0, PHP 7, PHP 8)

readlinecallbackhandlerremove — Видаляє раніше зареєстровану callback-функцію та відновлює термінал

### Опис

```methodsynopsis
readline_callback_handler_remove(): bool
```

Видаляє раніше зареєстровану callback-функцію та відновлює налаштування терміналу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо видалення пройшло успішно або **`false`**, якщо видаляти нічого.

### Приклади

Приклад використання інтерфейсу callback-функцій readline дивіться на сторінці опису функції [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.html)

### Дивіться також

-   [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.html) - Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління
-   [readlinecallbackreadchar()](function.readline-callback-read-char.html) - Читає символ та інформує callback-функцію readline, що отримано рядок