Виключення парсера FFI

-   [« FFIException](class.ffi-exception.html)
    
-   [OPcache »](book.opcache.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](book.ffi.html)
    
-   Виключення парсера FFI
    

# Виключення парсера FFI

(PHP 7> = 7.4.0, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class FFI\ParserException
     

     
      extends
       FFI\Exception
     
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