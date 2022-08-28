Створює екземпляр класу з переданими аргументами

-   [« ReflectionClass::isUserDefined](reflectionclass.isuserdefined.html)
    
-   [ReflectionClass::newInstanceArgs »](reflectionclass.newinstanceargs.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Створює екземпляр класу з переданими аргументами
    

# ReflectionClass::newInstance

(PHP 5, PHP 7, PHP 8)

ReflectionClass::newInstance — Створює екземпляр класу з переданими аргументами

### Опис

```methodsynopsis
public ReflectionClass::newInstance(mixed ...$args): object
```

Створює новий екземпляр класу. Прийняті аргументи передаються конструктор класу.

### Список параметрів

`args`

Приймає довільну кількість аргументів, подібно до функції [call\_user\_func()](function.call-user-func.html), які потім передаються конструктор класу.

### Значення, що повертаються

### Помилки

Якщо конструктор не є загальнодоступним (public), це призведе до викидання винятку [ReflectionException](class.reflectionexception.html)

Якщо конструктор відсутня, а параметр `args` має один і більше аргументів, то це призведе до викидання винятку [ReflectionException](class.reflectionexception.html)

### Дивіться також

-   [ReflectionClass::newInstanceArgs()](reflectionclass.newinstanceargs.html) - Створює екземпляр класу з переданими параметрами
-   [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.html) - Створює новий екземпляр класу без виклику конструктора