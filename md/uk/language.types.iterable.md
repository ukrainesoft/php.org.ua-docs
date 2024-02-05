---
navigation:
  - language.types.value.md: Типи значень
  - language.types.declarations.md: Оголошення типів »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Ітеровані
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Ітеровані

[Iterable](language.types.iterable.md) - це вбудований псевдонім типу часу компіляції для `array|Traversable`. З моменту появи в PHP 7.1.0 і до PHP 8.2.0 тип [iterable](language.types.iterable.md) був вбудованим псевдотипом, який діяв як названий псевдотип типу і його можна було вказувати як оголошення типу. Тип iterable можна використовувати в [foreach](control-structures.foreach.md) та з конструкцією **yield from**внутри[генератора](language.generators.md)

> **Зауваження** :
> 
> функцій-[генераторам](language.generators.md) як повертаний тип можна також вказувати тип iterable.
> 
> **Приклад #1 Приклад використання типу iterable, що повертається, для ітерованого генератора**
> 
> ```php
> <?php
> 
> function gen(): iterable {
>     yield 1;
>     yield 2;
>     yield 3;
> }
> 
> ?>
> ```
