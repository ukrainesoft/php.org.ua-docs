Клас ReflectionException

-   [« Reflector::toString](reflector.tostring.html)
    
-   [Обработка переменных »](book.var.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionException
    

# Клас ReflectionException

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас ReflectionException.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionException
     

     
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