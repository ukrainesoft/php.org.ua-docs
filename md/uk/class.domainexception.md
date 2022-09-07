---
navigation:
  - class.badmethodcallexception.md: « BadMethodCallException
  - class.invalidargumentexception.md: InvalidArgumentException »
  - index.md: PHP Manual
  - spl.exceptions.md: Исключения
title: Клас DomainException
---
# Клас DomainException

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Створюється виняток, якщо значення не відповідає певній допустимій області даних.

## Огляд класів

```classsynopsis

     
    

    
     
      class DomainException
     

     
      extends
       LogicException
     
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
