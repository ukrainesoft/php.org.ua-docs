---
navigation:
  - reserved.keywords.html: « Список ключових слів
  - reserved.constants.html: Обумовлені константи »
  - index.html: PHP Manual
  - reserved.html: Список зарезервованих слів
title: Обумовлені класи
---
## Обумовлені класи

У цьому розділі перераховуються стандартні визначені класи. Різноманітні модулі визначають інші класи, які описані у відповідній довідковій інформації.

### Стандартні певні класи

Ці класи визначені разом зі стандартним набором функцій, що йдуть зі збиранням PHP.

[Directory](class.directory.md)

Створюється функцією [dir()](function.dir.md)

**stdClass**

Створюється [приведенням типу до об'єкту](language.types.object.html#language.types.object.casting)

**PHPIncompleteClass**

Можливо, створюється функцією [unserialize()](function.unserialize.md)

[Exception](class.exception.md)

[ErrorException](class.errorexception.md)

[phpuserfilter](class.php-user-filter.md)

[Closure](class.closure.md)

Обумовлений остаточний клас [Closure](class.closure.html), використовується для внутрішньої реалізації [анонімних функцій](functions.anonymous.md)

[Generator](class.generator.md)

Обумовлений остаточний клас [Generator](class.generator.html), використовується для подання [генераторів](language.generators.md)

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

[Текущий класс](language.oop5.paamayim-nekudotayim.md)

**static**

[Поточний клас під час виконання](language.oop5.late-static-bindings.md)

**parent**

[Батьківський клас](language.oop5.paamayim-nekudotayim.md)
