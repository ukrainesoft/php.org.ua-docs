---
navigation:
  - random-engine-xoshiro256starstar.unserialize.md: '« Random\\Engine\\Xoshiro256StarStar::\_\_unserialize'
  - class.random-brokenrandomengineerror.md: Random\\BrokenRandomEngineError »
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\RandomError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\RandomError

(PHP 8 >= 8.2.0)

## Вступ

Базовий клас для помилок [Error](class.error.md), що виникають під час генерації або використання випадкової послідовності.

## Огляд класів

```classsynopsis

    
     class Random\RandomError
    

    
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
    
   public Error::__construct(string $message = "", int $code = 0, ?Throwable $previous = null)

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
