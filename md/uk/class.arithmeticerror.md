ArithmeticError

-   [« ArgumentCountError](class.argumentcounterror.html)
    
-   [AssertionError »](class.assertionerror.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые исключения](reserved.exceptions.html)
    
-   ArithmeticError
    

# ArithmeticError

(PHP 7, PHP 8)

## Вступ

**ArithmeticError** викидається, коли виникає помилка під час виконання математичних операцій. Такі помилки можна спровокувати побітовим зміщенням на негативне значення або викликом функції [intdiv()](function.intdiv.html), що приводить значення, що не входить до допустимого інтервалу цілих чисел (int).

## Огляд класів

```classsynopsis

     
    

    
     
      class ArithmeticError
     

     
      extends
       Error
     
     {

    /* Наследуемые свойства */
    
     protected
     string
      $message = "";
private
     string
      $string = "";
protected
     int
      $code;
protected
     string
      $file = "";
protected
     int
      $line;
private
     array
      $trace = [];
private
     ?Throwable
      $previous = null;


    /* Наследуемые методы */
    
   final public Error::getMessage(): string
final public Error::getPrevious(): ?Throwable
final public Error::getCode(): int
final public Error::getFile(): string
final public Error::getLine(): int
final public Error::getTrace(): array
final public Error::getTraceAsString(): string
public Error::__toString(): string
private Error::__clone(): void

   }
```