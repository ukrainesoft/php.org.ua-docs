---
navigation:
  - class.ui-key.html: « UIKey
  - class.ui-exception-runtimeexception.html: ОЙExceptionRuntimeException »
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: InvalidArgumentException
---
# InvalidArgumentException

(UI 1.0.3)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class UI\Exception\InvalidArgumentException
     

     
      extends
       InvalidArgumentException
     

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
