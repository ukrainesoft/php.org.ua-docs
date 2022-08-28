CompileError

-   [« DivisionByZeroError](class.divisionbyzeroerror.html)
    
-   [ParseError »](class.parseerror.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые исключения](reserved.exceptions.html)
    
-   CompileError
    

# CompileError

(PHP 7> 7.3.0, PHP 8)

## Вступ

Виняток **CompileError** викидається при деяких помилках компіляції, які раніше видавали фатальну помилку.

## Огляд класів

```classsynopsis

     
    

    
     
      class CompileError
     

     
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