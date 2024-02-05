---
navigation:
  - error.clone.md: '« Error::\_\_clone'
  - class.arithmeticerror.md: ArithmeticError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: ArgumentCountError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArgumentCountError

(PHP 7 >= PHP 7.1.0, PHP 8)

## Вступ

**ArgumentCountError** викидається, коли в метод користувача або функцію передано недостатню кількість аргументів.

Ця помилка також викидається, якщо в неваріативну вбудовану функцію передається дуже багато аргументів.

## Огляд класів

```classsynopsis

    
     class ArgumentCountError
    

    
     extends
      TypeError
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
