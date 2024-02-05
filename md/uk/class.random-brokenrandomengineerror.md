---
navigation:
  - class.random-randomerror.md: « Random\\RandomError
  - class.random-randomexception.md: Random\\RandomException »
  - index.md: PHP Manual
  - book.random.md: Random
title: Клас Random\\BrokenRandomEngineError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Random\\BrokenRandomEngineError

(PHP 8 >= 8.2.0)

## Вступ

Вказує, що об'єкт, що використовується [Random\\Engine](class.random-engine.md) зламаний, наприклад, тому що він сильно зміщений.

## Огляд класів

```classsynopsis

    
     class Random\BrokenRandomEngineError
    

    
     extends
      Random\RandomError
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
