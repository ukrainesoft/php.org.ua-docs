DivisionByZeroError

-   [« AssertionError](class.assertionerror.html)
    
-   [CompileError »](class.compileerror.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые исключения](reserved.exceptions.html)
    
-   DivisionByZeroError
    

# DivisionByZeroError

(PHP 7, PHP 8)

## Вступ

**DivisionByZeroError** викидається при спробі поділити число на нуль.

## Огляд класів

```classsynopsis

     
    

    
     
      class DivisionByZeroError
     

     
      extends
       ArithmeticError
     
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