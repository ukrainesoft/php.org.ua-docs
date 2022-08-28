Створює новий екземпляр класу без виклику конструктора

-   [« ReflectionClass::newInstanceArgs](reflectionclass.newinstanceargs.html)
    
-   [ReflectionClass::setStaticPropertyValue »](reflectionclass.setstaticpropertyvalue.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionClass](class.reflectionclass.html)
    
-   Створює новий екземпляр класу без виклику конструктора
    

# ReflectionClass::newInstanceWithoutConstructor

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionClass::newInstanceWithoutConstructor — Створює новий екземпляр класу без виклику конструктора

### Опис

```methodsynopsis
public ReflectionClass::newInstanceWithoutConstructor(): object
```

Створює новий екземпляр класу без виклику конструктора.

### Список параметрів

### Значення, що повертаються

### Помилки

Якщо клас є вбудованим, і його екземпляр не може бути створений без виклику конструктора, це призведе до генерації виключення [ReflectionException](class.reflectionexception.html). Цей виняток обмежений лише класами з модифікатором [final](language.oop5.final.html)

### Дивіться також

-   [ReflectionClass::newInstance()](reflectionclass.newinstance.html) - створює екземпляр класу з переданими аргументами
-   [ReflectionClass::newInstanceArgs()](reflectionclass.newinstanceargs.html) - Створює екземпляр класу з переданими параметрами