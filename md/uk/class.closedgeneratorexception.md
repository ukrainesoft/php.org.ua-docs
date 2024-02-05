---
navigation:
  - errorexception.getseverity.md: '« ErrorException::getSeverity'
  - class.error.md: Error »
  - index.md: PHP Manual
  - reserved.exceptions.md: Обумовлені винятки
title: Клас ClosedGeneratorException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ClosedGeneratorException

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

## Вступ

Исключение**ClosedGeneratorException** викидається при спробі отримати значення із закритого ітератора, реалізованого класом [Generator](class.generator.md)

## Огляд класів

```classsynopsis

    
     class ClosedGeneratorException
    

    
     extends
      Exception
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
