---
navigation:
  - class.luasandboxmemoryerror.md: « LuaSandboxMemoryError
  - class.luasandboxsyntaxerror.md: LuaSandboxSyntaxError »
  - index.md: PHP Manual
  - book.luasandbox.md: LuaSandbox
title: Клас LuaSandboxRuntimeError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас LuaSandboxRuntimeError

(PECL luasandbox >= 1.0.0)

## Вступ

Винятки, що відловлюються під час виконання LuaSandbox.

Їх можна відловити всередині Lua, використовуючи `pcall()`или`xpcall()`

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxRuntimeError
     

     
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
