---
navigation:
  - pharfileinfo.setmetadata.md: '« PharFileInfo::setMetadata'
  - book.rar.md: Rar »
  - index.md: PHP Manual
  - book.phar.md: Phar
title: Клас PharException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PharException

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

## Вступ

Клас PharException надає клас виключення модуля phar для блоків try/catch.

## Огляд класів

```classsynopsis

    
     class PharException
    

    
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
