---
navigation:
  - class.badfunctioncallexception.html: « BadFunctionCallException
  - class.domainexception.html: DomainException »
  - index.html: PHP Manual
  - spl.exceptions.html: Исключения
title: Клас BadMethodCallException
---
# Клас BadMethodCallException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Створюється виняток, якщо callback-функція відноситься до невизначеного методу або деякі аргументи відсутні.

## Огляд класів

```classsynopsis

     
    

    
     
      class BadMethodCallException
     

     
      extends
       BadFunctionCallException
     
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
