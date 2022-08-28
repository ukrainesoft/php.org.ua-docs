Клас LuaSandboxTimeoutError

-   [« LuaSandboxSyntaxError](class.luasandboxsyntaxerror.html)
    
-   [Misc. »](book.misc.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](book.luasandbox.html)
    
-   Клас LuaSandboxTimeoutError
    

# Клас LuaSandboxTimeoutError

(PECL luasandbox >= 1.0.0)

## Вступ

Виняток виникає при перевищенні настроєного ліміту часу центрального процесора (CPU).

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxTimeoutError
     

     
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

## Дивіться також

-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.html)