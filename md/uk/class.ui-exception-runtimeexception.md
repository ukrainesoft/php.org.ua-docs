---
navigation:
  - class.ui-exception-invalidargumentexception.md: « UI\\Exception\\InvalidArgumentException
  - faq.md: ЧАВО »
  - index.md: PHP Manual
  - book.ui.md: UI
title: RuntimeException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RuntimeException

(UI 1.0.3)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class UI\Exception\RuntimeException
     

     
      extends
       RuntimeException
     

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
