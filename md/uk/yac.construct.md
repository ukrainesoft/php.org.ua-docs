Конструктор класу

-   [« Yac::add](yac.add.html)
    
-   [Yac::delete »](yac.delete.html)
    
-   [PHP Manual](index.html)
    
-   [Yac](class.yac.html)
    
-   Конструктор класу
    

# Yac::construct

(PECL yac >= 1.0.0)

Yac::construct - Конструктор класу

### Опис

public **Yac::construct**(string `$prefix` = "")

Префікс використовується для додавання ключів, його можна використовувати для запобігання конфліктам між додатками.

### Список параметрів

`prefix`

Префікс (string)

### Помилки

Викидає [Exception](class.exception.html), якщо Yac не включено. Викидає [Exception](class.exception.html), якщо `prefix` перевищує максимальну довжину ключа 48 (**`YAC_MAX_KEY_LEN`**) байтів.