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

[Directory](class.directory.html)

Створюється функцією [dir()](function.dir.html)

**stdClass**

Створюється [приведенням типу до об'єкту](language.types.object.html#language.types.object.casting)

**PHPIncompleteClass**

Можливо, створюється функцією [unserialize()](function.unserialize.html)

[Exception](class.exception.html)

[ErrorException](class.errorexception.html)

[phpuserfilter](class.php-user-filter.html)

[Closure](class.closure.html)

Обумовлений остаточний клас [Closure](class.closure.html), використовується для внутрішньої реалізації [анонімних функцій](functions.anonymous.html)

[Generator](class.generator.html)

Обумовлений остаточний клас [Generator](class.generator.html), використовується для подання [генераторів](language.generators.html)

[ArithmeticError](class.arithmeticerror.html)

[AssertionError](class.assertionerror.html)

[DivisionByZeroError](class.divisionbyzeroerror.html)

[Error](class.error.html)

[Throwable](class.throwable.html)

[ParseError](class.parseerror.html)

[TypeError](class.typeerror.html)

### Спеціальні класи

Наступні ідентифікатори не можуть використовуватися як ім'я класу, тому що у них є спеціальне призначення.

**self**

[Текущий класс](language.oop5.paamayim-nekudotayim.html)

**static**

[Поточний клас під час виконання](language.oop5.late-static-bindings.html)

**parent**

[Батьківський клас](language.oop5.paamayim-nekudotayim.html)
