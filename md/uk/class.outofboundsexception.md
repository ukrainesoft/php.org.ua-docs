---
navigation:
  - class.logicexception.md: « LogicException
  - class.outofrangeexception.md: OutOfRangeException »
  - index.md: PHP Manual
  - spl.exceptions.md: Винятки
title: Клас OutOfBoundsException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас OutOfBoundsException

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Викидається виняток, якщо значення не є дійсним ключем. Це є помилками, які не можуть бути виявлені під час компіляції.

## Огляд класів

```classsynopsis

    
     class OutOfBoundsException
    

    
     extends
      RuntimeException
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
