Клонувати виняток

-   [« Exception::toString](exception.tostring.html)
    
-   [ErrorException »](class.errorexception.html)
    
-   [PHP Manual](index.html)
    
-   [Exception](class.exception.html)
    
-   Клонувати виняток
    

# Exception::clone

(PHP 5, PHP 7, PHP 8)

Exception::clone — Клонувати виняток

### Опис

```methodsynopsis
private Exception::__clone(): void
```

Намагається клонувати виняток, що призводить до фатальної помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Винятки *не* піддаються клонуванню.

### список змін

| Версия | Описание                                                     |
|--------|--------------------------------------------------------------|
|        | Метод **Exception::clone()** більше не є остаточним (final). |