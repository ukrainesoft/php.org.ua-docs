---
navigation:
  - class.luasandboxsyntaxerror.md: « LuaSandboxSyntaxError
  - book.misc.md: Misc. »
  - index.md: PHP Manual
  - book.luasandbox.md: LuaSandbox
title: Клас LuaSandboxTimeoutError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.md)
