---
navigation:
  - ffi-ctype.getstructfieldtype.md: '« FFICType::getStructFieldType'
  - class.ffi-parserexception.md: FFIParserException »
  - index.md: PHP Manual
  - book.ffi.md: FFI
title: Винятки FFI
---
# Винятки FFI

(PHP 7> = 7.4.0, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class FFI\Exception
     

     
      extends
       Error
     
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
    
   final public Error::getMessage(): string
final public Error::getPrevious(): ?Throwable
final public Error::getCode(): int
final public Error::getFile(): string
final public Error::getLine(): int
final public Error::getTrace(): array
final public Error::getTraceAsString(): string
public Error::__toString(): string
private Error::__clone(): void

   }
```
