---
navigation:
  - compersisthelper.savetostream.md: '« COMPersistHelper::SaveToStream'
  - class.com-safearray-proxy.md: com\_safearray\_proxy »
  - index.md: PHP Manual
  - book.com.md: COM
title: Клас com\_exception
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас com\_exception

(PHP 5, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

    
     final
     class com_exception
    

    
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
