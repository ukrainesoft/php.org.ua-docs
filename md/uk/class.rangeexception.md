Клас RangeException

-   [« OverflowException](class.overflowexception.html)
    
-   [RuntimeException »](class.runtimeexception.html)
    
-   [PHP Manual](index.html)
    
-   [Исключения](spl.exceptions.html)
    
-   Клас RangeException
    

# Клас RangeException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Викидається виняток, щоб вказати помилки діапазону під час виконання програми. Як правило, це означає, що була арифметична помилка, відмінна від недоповнення/переповнення. Це версія [DomainException](class.domainexception.html), призначена для виконання.

## Огляд класів

```classsynopsis

     
    

    
     
      class RangeException
     

     
      extends
       RuntimeException
     
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