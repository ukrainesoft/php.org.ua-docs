---
navigation:
  - class.assertionerror.md: « AssertionError
  - class.compileerror.md: CompileError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: DivisionByZeroError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DivisionByZeroError

(PHP 7, PHP 8)

## Вступ

**DivisionByZeroError** викидається при спробі поділити число на нуль.

## Огляд класів

```classsynopsis

     
      class DivisionByZeroError
     

     
      extends
       ArithmeticError
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
