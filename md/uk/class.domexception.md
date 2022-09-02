---
navigation:
  - domentityreference.construct.md: '« DOMEntityReference::construct'
  - class.domimplementation.md: DOMImplementation »
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMException
---
# Клас DOMException

(PHP 5, PHP 7, PHP 8)

## Вступ

Операції DOM за певних обставин викидають винятки, наприклад, коли виконання операції неможливе зі зрозумілих причин.

Дивіться також [Исключения](language.exceptions.md)

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class DOMException
     

     
      extends
       Exception
     
     {

    /* Свойства */
    
     public
     int
      $code;


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

## Властивості

code

Ціло число, що вказує тип помилки, що відбулася
