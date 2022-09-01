---
navigation:
  - function.sodium-unpad.html: « sodiumunpad
  - refs.database.md: Модулі для роботи з базами даних
  - index.md: PHP Manual
  - book.sodium.md: Sodium
title: Клас SodiumException
---
# Клас SodiumException

(PHP 7> = 7.2.0, PHP 8)

## Вступ

Винятки, що викидаються функціями sodium.

## Огляд класів

```classsynopsis

     
    

    
     
      class SodiumException
     

     
      extends
       Exception
     
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
