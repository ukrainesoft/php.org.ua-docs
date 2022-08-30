Помилки у PHP 7

-   [« Основы](language.errors.basics.html)
    
-   [Исключения »](language.exceptions.html)
    
-   [PHP Manual](index.html)
    
-   [Ошибки](language.errors.html)
    
-   Помилки у PHP 7
    

## Помилки у PHP 7

У PHP 7 механізм повідомлення про помилки було сильно змінено. Традиційне сповіщення про помилку в PHP 5 було замінено на новий механізм, в якому більшість помилок викликаються за допомогою винятків класу [Error](class.error.html)

Як і звичайні винятки, винятки [Error](class.error.html) викликаються до появи першого відповідного блоку [`catch`](language.exceptions.html#language.exceptions.catch). Якщо відповідних блоків не передбачено, то буде викликано будь-якого обробника винятків, встановленого за допомогою [setexceptionhandler()](function.set-exception-handler.html). У разі відсутності оброблювача за замовчуванням, виняток буде конвертовано у фатальну помилку та буде оброблено як традиційна помилка.

Оскільки клас [Error](class.error.html) не успадковується від класу [Exception](class.exception.html), блок `catch (Exception $e) { ... }` для обробки неперехоплених винятків PHP 5 не може перехопити виключення [Error](class.error.html). Для їх перехоплення використовуйте блок `catch (Error $e) { ... }` або встановіть обробник виключень за допомогою [setexceptionhandler()](function.set-exception-handler.html)

### Ієрархія [Error](class.error.html)

-   [Throwable](class.throwable.html)
    -   [Error](class.error.html)
        -   [ArithmeticError](class.arithmeticerror.html)
            -   [DivisionByZeroError](class.divisionbyzeroerror.html)
        -   [AssertionError](class.assertionerror.html)
        -   [CompileError](class.compileerror.html)
            -   [ParseError](class.parseerror.html)
        -   [TypeError](class.typeerror.html)
            -   [ArgumentCountError](class.argumentcounterror.html)
        -   [ValueError](class.valueerror.html)
        -   [UnhandledMatchError](class.unhandledmatcherror.html)
        -   [FiberError](class.fibererror.html)
    -   [Exception](class.exception.html)