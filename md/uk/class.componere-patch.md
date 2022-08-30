Клас ComponerePatch

-   [« ComponereDefinition::getClosures](componere-definition.getclosures.html)
    
-   [ComponerePatch::construct »](componere-patch.construct.html)
    
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

-   [ComponerePatch::construct](componere-patch.construct.html) - Конструктор класу Patch
-   [ComponerePatch::apply](componere-patch.apply.html) - Додаток
-   [ComponerePatch::revert](componere-patch.revert.html) - Скасування
-   [ComponerePatch::isApplied](componere-patch.isapplied.html) — Визначення стану
-   [ComponerePatch::derive](componere-patch.derive.html) - Отримання патчу
-   [ComponerePatch::getClosure](componere-patch.getclosure.html) — Отримує замикання
-   [ComponerePatch::getClosures](componere-patch.getclosures.html) — Отримує замикання