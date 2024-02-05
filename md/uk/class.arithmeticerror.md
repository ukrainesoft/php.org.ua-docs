---
navigation:
  - class.argumentcounterror.md: « ArgumentCountError
  - class.assertionerror.md: AssertionError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: ArithmeticError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArithmeticError

(PHP 7, PHP 8)

## Вступ

**ArithmeticError** викидається, коли виникає помилка під час виконання математичних операцій. Такі помилки можна спровокувати побітовим зміщенням на негативне значення або викликом функції [intdiv()](function.intdiv.md), що приводить значення, що не входить до допустимого інтервалу цілих чисел (int).

## Огляд класів

```classsynopsis

     
      class ArithmeticError
     

     
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
