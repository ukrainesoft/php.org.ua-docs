---
navigation:
  - componere-definition.getclosures.md: '« ComponereDefinition::getClosures'
  - componere-patch.construct.md: 'ComponerePatch::construct »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас ComponerePatch
---
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

-   [ComponerePatch::construct](componere-patch.construct.md) - Конструктор класу Patch
-   [ComponerePatch::apply](componere-patch.apply.md) - Додаток
-   [ComponerePatch::revert](componere-patch.revert.md) - Скасування
-   [ComponerePatch::isApplied](componere-patch.isapplied.md) — Визначення стану
-   [ComponerePatch::derive](componere-patch.derive.md) - Отримання патчу
-   [ComponerePatch::getClosure](componere-patch.getclosure.md) — Отримує замикання
-   [ComponerePatch::getClosures](componere-patch.getclosures.md) — Отримує замикання
