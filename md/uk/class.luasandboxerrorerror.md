Клас LuaSandboxErrorError

-   [« LuaSandboxError](class.luasandboxerror.md)
    
-   [LuaSandboxFatalError »](class.luasandboxfatalerror.md)
    
-   [PHP Manual](index.md)
    
-   [LuaSandbox](book.luasandbox.md)
    
-   Клас LuaSandboxErrorError
    

# Клас LuaSandboxErrorError

(PECL luasandbox >= 1.0.0)

## Вступ

Виняток викидається, коли Lua виявляє помилку в обробнику помилок.

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxErrorError
     

     
      extends
       LuaSandboxFatalError
     
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