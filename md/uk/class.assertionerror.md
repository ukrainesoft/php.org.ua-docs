---
navigation:
  - class.arithmeticerror.md: « ArithmeticError
  - class.divisionbyzeroerror.md: DivisionByZeroError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: AssertionError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# AssertionError

(PHP 7, PHP 8)

## Вступ

**AssertionError** викидається, коли твердження, зроблене за допомогою [assert()](function.assert.md), зазнає невдачі.

## Огляд класів

```classsynopsis

     
      class AssertionError
     

     
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
