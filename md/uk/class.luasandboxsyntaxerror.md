---
navigation:
  - class.luasandboxruntimeerror.md: « LuaSandboxRuntimeError
  - class.luasandboxtimeouterror.md: LuaSandboxTimeoutError »
  - index.md: PHP Manual
  - book.luasandbox.md: LuaSandbox
title: Клас LuaSandboxSyntaxError
---
# Клас LuaSandboxSyntaxError

(PECL luasandbox >= 1.0.0)

## Вступ

Виняток виникає, коли код Lua не може бути проаналізований.

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxSyntaxError
     

     
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
