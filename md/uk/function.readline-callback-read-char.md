Читає символ та інформує callback-функцію readline, що отримано рядок

-   [« readlinecallbackhandlerremove](function.readline-callback-handler-remove.html)
    
-   [readlineclearhistory »](function.readline-clear-history.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Readline](ref.readline.html)
    
-   Читає символ та інформує callback-функцію readline, що отримано рядок
    

# readlinecallbackreadchar

(PHP 5> = 5.1.0, PHP 7, PHP 8)

readlinecallbackreadchar — Читає символ та інформує callback-функцію readline, що отримано рядок

### Опис

```methodsynopsis
readline_callback_read_char(): void
```

Читає введений користувачем символ. Коли рядок отримано, ця функція інформує callback-функцію інтерфейсу readline, задану за допомогою [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.html), що рядок готовий до введення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

Приклад використання інтерфейсу callback-функцій readline дивіться на сторінці опису функції [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.html)

### Дивіться також

-   [readlinecallbackhandlerinstall()](function.readline-callback-handler-install.html) - Ініціалізує callback-інтерфейс readline та термінал, друкує рядок запрошення та негайно повертає управління
-   [readlinecallbackhandlerremove()](function.readline-callback-handler-remove.html) - Видаляє раніше зареєстровану callback-функцію та відновлює термінал