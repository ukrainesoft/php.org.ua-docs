---
navigation:
  - class.invalidargumentexception.md: « InvalidArgumentException
  - class.logicexception.md: LogicException »
  - index.md: PHP Manual
  - spl.exceptions.md: Винятки
title: Клас LengthException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас LengthException

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Створюється виняток, якщо довжина неприпустима.

## Огляд класів

```classsynopsis

    
     class LengthException
    

    
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
