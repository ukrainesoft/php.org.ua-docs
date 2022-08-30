Визначення конструктора

-   [« ComponereDefinition](class.componere-definition.html)
    
-   [ComponereDefinition::addConstant »](componere-definition.addconstant.html)
    
-   [PHP Manual](index.html)
    
-   [ComponereDefinition](class.componere-definition.html)
    
-   Визначення конструктора
    

# ComponereDefinition::construct

(Componere 2 >= 2.1.0)

ComponereDefinition::construct - Визначення конструктора

### Опис

public **ComponereDefinition::construct**(string `$name`

public **ComponereDefinition::construct**(string `$name`, string `$parent`

public **ComponereDefinition::construct**(string `$name`, array `$interfaces`

public **ComponereDefinition::construct**(string `$name`, string `$parent`, array `$interfaces`

### Список параметрів

`name`

Реєстронезалежне ім'я класу

`parent`

Реєстронезалежне ім'я класу

`interfaces`

Масив реєстронезалежних імен класів

### Винятки

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо зроблено спробу замінити внутрішній клас

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо зроблено спробу замінити інтерфейс

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.html), якщо зроблено спробу замінити трейт

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо клас, зазначений у `interfaces` НЕ знайдений

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо клас, зазначений у `interfaces` не є інтерфейсом