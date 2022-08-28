Створити виняток

-   [« Exception](class.exception.html)
    
-   [Exception::getMessage »](exception.getmessage.html)
    
-   [PHP Manual](index.html)
    
-   [Exception](class.exception.html)
    
-   Створити виняток
    

# Exception::construct

(PHP 5, PHP 7, PHP 8)

Exception::construct — Створити виняток

### Опис

public **Exception::construct**(string `$message` = "", int `$code` [Throwable](class.throwable.html) `$previous` **`null`**

Створює виняток.

### Список параметрів

`message`

Текст повідомлення.

`code`

Код виключення.

`previous`

Попередній виняток. Використовується для створення ланцюжка винятків.

> **Зауваження**: Виклик конструктора класу Exception з його підкласу, ігнорує аргументи за умовчанням, якщо властивості $code та $message вже встановлені.

### Примітки

> **Зауваження**
> 
> Параметр `message` *не* є бінарно-безпечним.