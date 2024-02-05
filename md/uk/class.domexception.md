---
navigation:
  - domentityreference.construct.md: '« DOMEntityReference::\_\_construct'
  - class.domimplementation.md: DOMImplementation »
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMException

(PHP 5, PHP 7, PHP 8)

## Вступ

Операції DOM іноді викидають винятки, наприклад, коли виконання операції неможливе з нез'ясованих причин.

Смотрите также[Винятки](language.exceptions.md)

## Огляд класів

```classsynopsis

     
      final
      class DOMException
     

     
      extends
       Exception
      {

     /* Свойства */
     
      public
      int
       $code;


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

## Властивості

code

Ціле число, яке вказує тип згенерованої помилки.
