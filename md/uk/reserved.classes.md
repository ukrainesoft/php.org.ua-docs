---
navigation:
  - reserved.keywords.md: « Список ключових слів
  - reserved.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - reserved.md: Список зарезервованих слів
title: Обумовлені класи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Обумовлені класи

У цьому розділі перераховуються стандартні визначені класи. Різноманітні модулі визначають інші класи, які описані у відповідній довідковій інформації.

### Стандартні певні класи

Ці класи визначені разом зі стандартним набором функцій, що йдуть зі збиранням PHP.

[Directory](class.directory.md)

Створюється функцією [dir()](function.dir.md)

[stdClass](class.stdclass.md)

Порожній клас загального призначення, створений у результаті [перетворення на об'єкт](language.types.object.md#language.types.object.casting) або різні стандартні функції.

**\_\_PHP\_Incomplete\_Class**

Можливо, створюється функцією [unserialize()](function.unserialize.md)

[Exception](class.exception.md)

[ErrorException](class.errorexception.md)

[php\_user\_filter](class.php-user-filter.md)

[Closure](class.closure.md)

Обумовлений остаточний клас [Closure](class.closure.md), используется для внутренней реализации[анонімних функцій](functions.anonymous.md)

[Generator](class.generator.md)

Обумовлений остаточний клас [Generator](class.generator.md), используется для представления[генераторів](language.generators.md)

[ArithmeticError](class.arithmeticerror.md)

[AssertionError](class.assertionerror.md)

[DivisionByZeroError](class.divisionbyzeroerror.md)

[Error](class.error.md)

[Throwable](class.throwable.md)

[ParseError](class.parseerror.md)

[TypeError](class.typeerror.md)

### Спеціальні класи

Наступні ідентифікатори не можуть використовуватися як ім'я класу, тому що у них є спеціальне призначення.

**self**

[Поточний клас](language.oop5.paamayim-nekudotayim.md)

**static**

[Поточний клас під час виконання](language.oop5.late-static-bindings.md)

**parent**

[Батьківський клас](language.oop5.paamayim-nekudotayim.md)
