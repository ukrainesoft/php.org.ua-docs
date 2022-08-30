Клас comexception

-   [« COMPersistHelper::SaveToStream](compersisthelper.savetostream.md)
    
-   [Функции COM »](ref.com.md)
    
-   [PHP Manual](index.md)
    
-   [COM](book.com.md)
    
-   Клас comexception
    

# Клас comexception

(PHP 5, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class com_exception
     

     
      extends
       Exception
     

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