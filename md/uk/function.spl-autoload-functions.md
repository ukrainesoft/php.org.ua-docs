Отримання списку всіх зареєстрованих функцій autoload()

-   [« spl\_autoload\_extensions](function.spl-autoload-extensions.html)
    
-   [spl\_autoload\_register »](function.spl-autoload-register.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SPL](ref.spl.html)
    
-   Отримання списку всіх зареєстрованих функцій autoload()
    

# splautoloadфункцій

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoloadfunctions — отримання списку всіх зареєстрованих функцій autoload()

### Опис

```methodsynopsis
spl_autoload_functions(): array
```

Отримує список усіх зареєстрованих функцій autoload().

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) всіх зареєстрованих у autoload функцій. Якщо черга автозавантаження не активована, поверне **`false`**. Якщо жодна функція не зареєстрована, поверне порожній масив.