Клас LuaSandboxFatalError

-   [« LuaSandboxErrorError](class.luasandboxerrorerror.html)
    
-   [LuaSandboxMemoryError »](class.luasandboxmemoryerror.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](book.luasandbox.html)
    
-   Клас LuaSandboxFatalError
    

# Клас LuaSandboxFatalError

(PECL luasandbox >= 1.0.0)

## Вступ

Невідловлювані винятки LuaSandbox.

Їх не можна відловити всередині Lua за допомогою `pcall()` або `xpcall()`

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxFatalError
     

     
      extends
       LuaSandboxError
     
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