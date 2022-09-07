---
navigation:
  - class.parle-errorinfo.md: « ParleErrorInfo
  - class.parle-parserexception.md: ParleParserException »
  - index.md: PHP Manual
  - book.parle.md: Parle
title: Клас ParleLexerException
---
# Клас ParleLexerException

(PECL parle >= 0.5.1)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Parle\LexerException
     

     
      extends
       Exception
     

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



    /* Методы */
    
    

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
