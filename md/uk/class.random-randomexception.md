---
navigation:
  - class.random-brokenrandomengineerror.md: « Random\\BrokenRandomEngineError
  - book.seaslog.md: Seaslog »
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\RandomException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\RandomException

(PHP 8 >= 8.2.0)

## Вступ

Базовий клас для винятків [Exception](class.exception.md), що виникають під час генерації або використання випадкової послідовності.

## Огляд класів

```classsynopsis

    
     class Random\RandomException
    

    
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
    
   public Exception::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

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
