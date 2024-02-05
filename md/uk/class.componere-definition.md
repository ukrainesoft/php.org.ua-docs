---
navigation:
  - componere-abstract-definition.getreflector.md: '« Componere\\Abstract\\Definition::getReflector'
  - componere-definition.construct.md: 'Componere\\Definition::\_\_construct »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас Componere\\Definition
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Componere\\Definition

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

-   [Componere\\Definition::\_\_construct](componere-definition.construct.md) \- Визначення конструктора
-   [Componere\\Definition::addConstant](componere-definition.addconstant.md)— додає константу
-   [Componere\\Definition::addProperty](componere-definition.addproperty.md) \- Додає властивість
-   [Componere\\Definition::register](componere-definition.register.md) \- Реєстрація
-   [Componere\\Definition::isRegistered](componere-definition.isregistered.md)— Визначення стану
-   [Componere\\Definition::getClosure](componere-definition.getclosure.md)— Отримує замикання
-   [Componere\\Definition::getClosures](componere-definition.getclosures.md)— Отримує замикання
