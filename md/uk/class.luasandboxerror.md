---
navigation:
  - luasandboxfunction.dump.html: '« LuaSandboxFunction::dump'
  - class.luasandboxerrorerror.html: LuaSandboxErrorError »
  - index.html: PHP Manual
  - book.luasandbox.html: LuaSandbox
title: Клас LuaSandboxError
---
# Клас LuaSandboxError

(PECL luasandbox >= 1.0.0)

## Вступ

Базовий клас для винятків LuaSandbox

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxError
     

     
      extends
       Exception
     
     {

    /* Константы */
    
     const
     int
      RUN = 2;

    const
     int
      SYNTAX = 3;

    const
     int
      MEM = 4;

    const
     int
      ERR = 5;


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

## Обумовлені константи

**`LuaSandboxError::RUN`**

**`LuaSandboxError::SYNTAX`**

**`LuaSandboxError::MEM`**

**`LuaSandboxError::ERR`**
