Клонує помилку

-   [« Error::toString](error.tostring.html)
    
-   [ArgumentCountError »](class.argumentcounterror.html)
    
-   [PHP Manual](index.html)
    
-   [Error](class.error.html)
    
-   Клонує помилку
    

# Error::clone

(PHP 7, PHP 8)

Error::clone - Клонує помилку

### Опис

```methodsynopsis
private Error::__clone(): void
```

Об'єкт класу Error не можна клонувати, тому ця функція викликає фатальну помилку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Об'єкт класу Error *не можна* клонувати.

### список змін

| Версия | Описание |
| --- | --- |
|  | Метод **Error::clone()** більше не є остаточним (final). |