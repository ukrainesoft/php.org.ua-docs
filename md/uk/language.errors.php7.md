---
navigation:
  - language.errors.basics.md: « Основи
  - language.exceptions.md: Винятки »
  - index.md: PHP Manual
  - language.errors.md: Помилки
title: Помилки у PHP 7
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Помилки у PHP 7

У PHP 7 механізм повідомлення про помилки було сильно змінено. Традиційне сповіщення про помилку в PHP 5 було замінено на новий механізм, в якому більшість помилок викликаються за допомогою винятків класу [Error](class.error.md)

Як і звичайні винятки, винятки [Error](class.error.md) викликаються до появи першого відповідного блоку `catch`. Якщо відповідних блоків не передбачено, то буде викликано будь-якого обробника винятків, встановленого за допомогою [set\_exception\_handler()](function.set-exception-handler.md). У разі відсутності оброблювача за замовчуванням, виняток буде конвертовано у фатальну помилку та буде оброблено як традиційна помилка.

Оскільки клас [Error](class.error.md)не наследуется от класса[Exception](class.exception.md), блок`catch (Exception $e) { ... }` для обробки неперехоплених винятків PHP 5 не може перехопити виключення [Error](class.error.md)Для их перехвата используйте блок`catch (Error $e) { ... }`или установите обработчик исключений с помощью[set\_exception\_handler()](function.set-exception-handler.md)

### Иерархия[Error](class.error.md)

-   [Throwable](class.throwable.md)
    -   [Error](class.error.md)
        -   [ArithmeticError](class.arithmeticerror.md)
            -   [DivisionByZeroError](class.divisionbyzeroerror.md)
        -   [AssertionError](class.assertionerror.md)
        -   [CompileError](class.compileerror.md)
            -   [ParseError](class.parseerror.md)
        -   [TypeError](class.typeerror.md)
            -   [ArgumentCountError](class.argumentcounterror.md)
        -   [ValueError](class.valueerror.md)
        -   [UnhandledMatchError](class.unhandledmatcherror.md)
        -   [FiberError](class.fibererror.md)
    -   [Exception](class.exception.md)
        -   ...
