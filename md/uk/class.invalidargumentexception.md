---
navigation:
  - class.domainexception.md: « DomainException
  - class.lengthexception.md: LengthException »
  - index.md: PHP Manual
  - spl.exceptions.md: Винятки
title: Клас InvalidArgumentException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас InvalidArgumentException

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Створюється виняток, якщо аргумент відповідає очікуваному типу.

## Огляд класів

```classsynopsis

    
     class InvalidArgumentException
    

    
     extends
      LogicException
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
