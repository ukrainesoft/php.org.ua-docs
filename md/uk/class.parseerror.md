---
navigation:
  - class.compileerror.md: « CompileError
  - class.typeerror.md: TypeError »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: ParseError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ParseError

(PHP 7, PHP 8)

## Вступ

**ParseError** викидається, коли виникає помилка при розборі PHP-коду, наприклад, коли викликається функція [eval()](function.eval.md)

> **Зауваження**: Починаючи з PHP 7.3.0, клас **ParseError**наследуется от[CompileError](class.compileerror.md). Раніше цей клас розширював клас [Error](class.error.md)

## Огляд класів

```classsynopsis

    
     class ParseError
    

    
     extends
      CompileError
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
