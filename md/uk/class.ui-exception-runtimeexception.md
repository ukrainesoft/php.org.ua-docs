RuntimeException

-   [« UI\\Exception\\InvalidArgumentException](class.ui-exception-invalidargumentexception.html)
    
-   [ЧАВО »](faq.html)
    
-   [PHP Manual](index.html)
    
-   [UI](book.ui.html)
    
-   RuntimeException
    

# RuntimeException

(UI 1.0.3)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class UI\Exception\RuntimeException
     

     
      extends
       RuntimeException
     

     implements 
       Throwable {

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