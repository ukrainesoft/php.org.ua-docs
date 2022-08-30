UnhandledMatchError

-   [« ValueError](class.valueerror.md)
    
-   [FiberError »](class.fibererror.md)
    
-   [PHP Manual](index.md)
    
-   [Обумовлені винятки](reserved.exceptions.md)
    
-   UnhandledMatchError
    

# UnhandledMatchError

(PHP 8)

## Вступ

**UnhandledMatchError** викидається, якщо суб'єкт, переданий у вираз match, не обробляється жодною зі сторін виразу match.

## Огляд класів

```classsynopsis

     
    

    
     
      class UnhandledMatchError
     

     
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