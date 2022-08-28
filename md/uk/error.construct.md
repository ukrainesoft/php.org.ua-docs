Створює об'єкт класу Error

-   [« Error](class.error.html)
    
-   [Error::getMessage »](error.getmessage.html)
    
-   [PHP Manual](index.html)
    
-   [Error](class.error.html)
    
-   Створює об'єкт класу Error
    

# Error::construct

(PHP 7, PHP 8)

Error::construct — Створює об'єкт класу Error

### Опис

public **Error::construct**(string `$message` = "", int `$code` [Throwable](class.throwable.html) `$previous` **`null`**

Створює об'єкт класу Error.

### Список параметрів

`message`

Повідомлення про помилку.

`code`

Код помилки.

`previous`

Попередній об'єкт, що реалізує throwable інтерфейс, використовується для створення ланцюжка винятків.

### Примітки

> **Зауваження**
> 
> Значення `message` *НЕ* є безпечним для бінарних даних, тобто в тексті повідомлення не можна використовувати символ із кодом