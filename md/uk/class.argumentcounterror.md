ArgumentCountError

-   [« Error::clone](error.clone.md)
    
-   [ArithmeticError »](class.arithmeticerror.md)
    
-   [PHP Manual](index.md)
    
-   [Обумовлені винятки](reserved.exceptions.md)
    
-   ArgumentCountError
    

# ArgumentCountError

(PHP 7> = PHP 7.1.0, PHP 8)

## Вступ

**ArgumentCountError** викидається, коли в метод користувача або функцію передано недостатню кількість аргументів.

## Огляд класів

```classsynopsis

     
    

    
     
      class ArgumentCountError
     

     
      extends
       TypeError
     
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