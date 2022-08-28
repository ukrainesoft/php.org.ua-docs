Клас ComponereDefinition

-   [« Componere\\Abstract\\Definition::getReflector](componere-abstract-definition.getreflector.html)
    
-   [Componere\\Definition::\_\_construct »](componere-definition.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Componere](book.componere.html)
    
-   Клас ComponereDefinition
    

# Клас ComponereDefinition

(Componere 2 >= 2.1.0)

## Вступ

Клас Definition дозволяє програмісту створювати та реєструвати тип під час виконання.

Якщо Definition замінить існуючий клас, існуючий клас буде відновлено після знищення Definition.

## Огляд класів

```classsynopsis

     
    

    
    
     
      final
      class Componere\Definition
     

     
      extends
       Componere\Abstract\Definition
     
     {
    

    /* Конструкторы класса */
    
   public __construct(string $name)
public __construct(string $name, string $parent)
public __construct(string $name, array $interfaces)
public __construct(string $name, string $parent, array $interfaces)


    /* Методы */
    public addConstant(string $name, Componere\Value $value): Definition
public addProperty(string $name, Componere\Value $value): Definition
public register(): void
public isRegistered(): bool
public getClosure(string $name): Closure
public getClosures(): array


    /* Наследуемые методы */
    public Componere\Abstract\Definition::addInterface(string $interface): Definition
public Componere\Abstract\Definition::addMethod(string $name, Componere\Method $method): Definition
public Componere\Abstract\Definition::addTrait(string $trait): Definition
public Componere\Abstract\Definition::getReflector(): ReflectionClass


   }
```

## Зміст

-   [Componere\\Definition::\_\_construct](componere-definition.construct.html) - Визначення конструктора
-   [Componere\\Definition::addConstant](componere-definition.addconstant.html) — додає константу
-   [Componere\\Definition::addProperty](componere-definition.addproperty.html) - Додає властивість
-   [Componere\\Definition::register](componere-definition.register.html) - Реєстрація
-   [Componere\\Definition::isRegistered](componere-definition.isregistered.html) — Визначення стану
-   [Componere\\Definition::getClosure](componere-definition.getclosure.html) — Отримує замикання
-   [Componere\\Definition::getClosures](componere-definition.getclosures.html) — Отримує замикання