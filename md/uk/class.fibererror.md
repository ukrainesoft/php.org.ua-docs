FiberError

-   [« UnhandledMatchError](class.unhandledmatcherror.md)
    
-   [Вбудовані інтерфейси та класи »](reserved.interfaces.md)
    
-   [PHP Manual](index.md)
    
-   [Обумовлені винятки](reserved.exceptions.md)
    
-   FiberError
    

# FiberError

(PHP 8> = 8.1.0)

## Вступ

**FiberError** викидає, якщо в об'єкті [Fiber](class.fiber.md) виконується неприпустима операція.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class FiberError
     

     
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


    /* Методы */
    

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