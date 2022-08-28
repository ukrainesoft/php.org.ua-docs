Повертає код виключення

-   [« Throwable::getMessage](throwable.getmessage.html)
    
-   [Throwable::getFile »](throwable.getfile.html)
    
-   [PHP Manual](index.html)
    
-   [Throwable](class.throwable.html)
    
-   Повертає код виключення
    

# Throwable::getCode

(PHP 7, PHP 8)

Throwable::getCode — Повертає код виключення

### Опис

```methodsynopsis
public Throwable::getCode(): int
```

Повертає код помилки викинутого об'єкта, до якого застосовано функцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код виключення у вигляді цілого числа (int) [Exception](class.exception.html), але можливий і інший тип, що повертається в класах, що успадковують [Exception](class.exception.html) (наприклад, у вигляді рядка (string), якщо тип помилки [PDOException](class.pdoexception.html)

### Дивіться також

-   [Exception::getCode()](exception.getcode.html) - Отримує код виключення