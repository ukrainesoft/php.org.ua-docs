---
navigation:
  - class.luasandboxfatalerror.md: « LuaSandboxFatalError
  - class.luasandboxruntimeerror.md: LuaSandboxRuntimeError »
  - index.md: PHP Manual
  - book.luasandbox.md: LuaSandbox
title: Клас LuaSandboxMemoryError
---
# Клас LuaSandboxMemoryError

(PECL luasandbox >= 1.0.0)

## Вступ

Виняток викидається, коли Lua може виділити пам'ять.

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxMemoryError
     

     
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

-   [LuaSandbox::setMemoryLimit()](luasandbox.setmemorylimit.md)
