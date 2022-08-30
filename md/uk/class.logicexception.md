Клас LogicException

-   [« LengthException](class.lengthexception.md)
    
-   [OutOfBoundsException »](class.outofboundsexception.md)
    
-   [PHP Manual](index.md)
    
-   [Исключения](spl.exceptions.md)
    
-   Клас LogicException
    

# Клас LogicException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Виняток, який представляє помилку в логіці програми. Такий тип винятків повинен безпосередньо призвести до виправлення у вашому коді.

## Огляд класів

```classsynopsis

     
    

    
     
      class LogicException
     

     
      extends
       Exception
     
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
    
   final public Exception::getMessage(): string
final public Exception::getPrevious(): ?Throwable
final public Exception::getCode(): int
final public Exception::getFile(): string
final public Exception::getLine(): int
final public Exception::getTrace(): array
final public Exception::getTraceAsString(): string
public Exception::__toString(): string
private Exception::__clone(): void

   }
```