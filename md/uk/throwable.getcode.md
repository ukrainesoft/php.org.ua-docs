Повертає код виключення

-   [« Throwable::getMessage](throwable.getmessage.md)
    
-   [Throwable::getFile »](throwable.getfile.md)
    
-   [PHP Manual](index.md)
    
-   [Throwable](class.throwable.md)
    
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

Повертає код виключення у вигляді цілого числа (int) [Exception](class.exception.md), але можливий і інший тип, що повертається в класах, що успадковують [Exception](class.exception.md) (наприклад, у вигляді рядка (string), якщо тип помилки [PDOException](class.pdoexception.md)

### Дивіться також

-   [Exception::getCode()](exception.getcode.md) - Отримує код виключення