Спроба завантажити клас усіма зареєстрованими функціями autoload()

-   [« iterator\_to\_array](function.iterator-to-array.html)
    
-   [spl\_autoload\_extensions »](function.spl-autoload-extensions.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SPL](ref.spl.html)
    
-   Спроба завантажити клас усіма зареєстрованими функціями autoload()
    

# splautoloadcall

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoloadcall — Спроба завантажити клас усіма зареєстрованими функціями autoload()

### Опис

```methodsynopsis
spl_autoload_call(string $class): void
```

Цю функцію можна використовувати для ручного пошуку класу або інтерфейсу, використовуючи всі зареєстровані методи autoload.

### Список параметрів

`class`

Ім'я класу, що шукається.

### Значення, що повертаються

Функція не повертає значення після виконання.