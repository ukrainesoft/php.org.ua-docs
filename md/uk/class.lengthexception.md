Клас LengthException

-   [« InvalidArgumentException](class.invalidargumentexception.md)
    
-   [LogicException »](class.logicexception.md)
    
-   [PHP Manual](index.md)
    
-   [Исключения](spl.exceptions.md)
    
-   Клас LengthException
    

# Клас LengthException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Створюється виняток, якщо довжина неприпустима.

## Огляд класів

```classsynopsis

     
    

    
     
      class LengthException
     

     
      extends
       LogicException
     
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