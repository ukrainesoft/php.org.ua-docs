Додає метод

-   [« Componere\\Abstract\\Definition::addInterface](componere-abstract-definition.addinterface.html)
    
-   [Componere\\Abstract\\Definition::addTrait »](componere-abstract-definition.addtrait.html)
    
-   [PHP Manual](index.html)
    
-   [Componere\\Abstract\\Definition](class.componere-abstract-definition.html)
    
-   Додає метод
    

# ComponereAbstractDefinition::addMethod

(Componere 2 >= 2.1.0)

ComponereAbstractDefinition::addMethod — Додає метод

### Опис

```methodsynopsis
public Componere\Abstract\Definition::addMethod(string $name, Componere\Method $method): Definition
```

Повинен створити чи перевизначити метод у поточному визначенні.

### Список параметрів

`name`

Нечутливе до регістру ім'я методу

`method`

[Componere\\Method](class.componere-method.html) раніше не доданий до іншого Definition

### Значення, що повертаються

The current Definition

### Exceptions

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо Definition було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.html), якщо метод був доданий до іншого визначення