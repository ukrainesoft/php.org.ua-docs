Повертає код помилки для останньої операції FDF

-   [« fdfenumvalues](function.fdf-enum-values.html)
    
-   [fdferror »](function.fdf-error.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](ref.fdf.html)
    
-   Повертає код помилки для останньої операції FDF
    

# fdferrno

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdferrno — Повертає код помилки для останньої операції FDF

### Опис

```methodsynopsis
fdf_errno(): int
```

Отримує код помилки, встановлений останнім викликом функції FDF.

Текстовий опис помилки можна отримати за допомогою [fdferror()](function.fdf-error.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повернення коду помилки як ціле число або нуль, якщо помилок не було.

### Дивіться також

-   [fdferror()](function.fdf-error.html) - Повертає опис помилки для коду помилки FDF