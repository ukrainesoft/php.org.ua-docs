---
navigation:
  - class.ui-key.md: « UI\\Key
  - class.ui-exception-runtimeexception.md: UI\\Exception\\RuntimeException »
  - index.md: PHP Manual
  - book.ui.md: UI
title: InvalidArgumentException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
