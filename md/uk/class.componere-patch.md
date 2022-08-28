Клас ComponerePatch

-   [« Componere\\Definition::getClosures](componere-definition.getclosures.html)
    
-   [Componere\\Patch::\_\_construct »](componere-patch.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Componere](book.componere.html)
    
-   Клас ComponerePatch
    

# Клас ComponerePatch

(Componere 2 >= 2.1.0)

## Вступ

Клас Patch дозволяє програмісту змінювати тип екземпляра під час виконання без реєстрації нового Definition.

Коли Patch знищується, він повертається, тому екземпляри, які були виправлені протягом терміну дії Patch, повертаються до їхнього формального типу.

## Огляд класів

```classsynopsis



    
     
      final
      class Componere\Patch
     

     
      extends
       Componere\Abstract\Definition
     
     {


    /* Конструкторы класса */
    
   public __construct(object $instance)
public __construct(object $instance, array $interfaces)


    /* Методы */
    public apply(): void
public revert(): void
public isApplied(): bool
public derive(object $instance): Patch
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

-   [Componere\\Patch::\_\_construct](componere-patch.construct.html) - Конструктор класу Patch
-   [Componere\\Patch::apply](componere-patch.apply.html) - Додаток
-   [Componere\\Patch::revert](componere-patch.revert.html) - Скасування
-   [Componere\\Patch::isApplied](componere-patch.isapplied.html) — Визначення стану
-   [Componere\\Patch::derive](componere-patch.derive.html) - Отримання патчу
-   [Componere\\Patch::getClosure](componere-patch.getclosure.html) — Отримує замикання
-   [Componere\\Patch::getClosures](componere-patch.getclosures.html) — Отримує замикання