---
navigation:
  - sqlite3.version.md: '« SQLite3::version'
  - class.sqlite3stmt.md: SQLite3Stmt »
  - index.md: PHP Manual
  - book.sqlite3.md: SQLite3
title: Клас SQLite3Exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SQLite3Exception

(PHP 8 >= 8.3.0)

## Вступ

Є винятком, специфічним для SQLite3.

## Огляд класів

```classsynopsis

    
     class SQLite3Exception
    

    
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
