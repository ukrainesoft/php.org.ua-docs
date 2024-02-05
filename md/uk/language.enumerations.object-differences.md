---
navigation:
  - language.enumerations.expressions.md: « Значення перерахування у постійних виразах
  - language.enumerations.listing.md: Список значень »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Відмінності від об'єктів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Відмінності від об'єктів

Хоча перерахування побудовані на класах та об'єктах, вони не підтримують повну об'єктно-пов'язану функціональність. Як приклад, варіантів перерахувань не дозволені стани.

-   Конструктори та деструктори заборонені.
-   Спадкування не підтримується. Перелікам не можна успадковувати або успадковуватись.
-   Статичні властивості чи властивості об'єкта не допускаються.
-   Клонування варіанта перерахування не підтримується, оскільки варіанти мають бути одноелементними екземплярами.
-   [Магические методы](language.oop5.magic.md) , крім наведених нижче, заборонені.
-   Переліки мають бути оголошені до початку роботи з ними.

Перелікам доступні такі функціональні можливості об'єкта з аналогічною поведінкою:

-   Методи public, private і protected.
-   Статичні методи public, private і protected.
-   Константи public, private і protected.
-   Перелікам дозволено продавати будь-яку кількість інтерфейсів.
-   До перерахувань та варіантів дозволено додавати[атрибути](language.attributes.md). Цільовий фільтр\*\*`TARGET_CLASS`**включає самі перерахування. Цільовий фільтр**`TARGET_CLASS_CONST`\*\*включає варіанти перерахувань.
-   Магічні методи[\_\_call](language.oop5.overloading.md#object.call) [\_\_callStatic](language.oop5.overloading.md#object.callstatic), и[\_\_invoke](language.oop5.magic.md#object.invoke)
-   Константи \*\*`__CLASS__`**и**`__FUNCTION__`\*\*поводяться як завжди.

Магічна константа `::class` для типу перерахування оцінюється як назва перерахування, включаючи будь-який простір імен, так само, як об'єкт. Магічна константа `::class` в екземплярі варіанта також оцінюється як тип перерахування, оскільки вона екземпляр цього типу.

Крім того, варіанти переліку не можна створювати через ключове слово `new` або методом [ReflectionClass::newInstanceWithoutConstructor()](reflectionclass.newinstancewithoutconstructor.md)Оба способа приведут к ошибке.

```php
<?php

$clovers = new Suit();
// Error: Cannot instantiate enum Suit

$horseshoes = (new ReflectionClass(Suit::class))->newInstanceWithoutConstructor()
// Error: Cannot instantiate enum Suit
?>
```
