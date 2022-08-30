Створює ReflectionClassConstant

-   [« ReflectionClassConstant](class.reflectionclassconstant.html)
    
-   [ReflectionClassConstant::export »](reflectionclassconstant.export.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClassConstant](class.reflectionclassconstant.html)
    
-   Створює ReflectionClassConstant
    

# ReflectionClassConstant::construct

(PHP 7> = 7.1.0, PHP 8)

ReflectionClassConstant::construct — Створює ReflectionClassConstant

### Опис

public **ReflectionClassConstant::construct**(object | string `$class`, string `$constant`

Створює новий об'єкт [ReflectionClassConstant](class.reflectionclassconstant.html)

### Список параметрів

`class`

Рядок (string), що містить ім'я класу для відображення, або об'єкт (object).

`constant`

Назва константи класу.

### Помилки

Викидає [Exception](class.exception.html) якщо передана константа класу немає.

### Дивіться також

-   [Конструктори](language.oop5.decon.html#language.oop5.decon.constructor)