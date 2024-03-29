---
navigation:
  - class.divisionbyzeroerror.md: « DivisionByZeroError
  - class.parseerror.md: ParseError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: CompileError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CompileError

(PHP 7 > 7.3.0, PHP 8)

## Вступ

Исключение**CompileError** викидається при деяких помилках компіляції, які раніше видавали фатальну помилку.

## Огляд класів

```classsynopsis

    
     class CompileError
    

    
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
