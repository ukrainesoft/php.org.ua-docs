---
navigation:
  - snmp.walk.md: '« SNMP::walk'
  - book.sockets.md: Сокети »
  - index.md: PHP Manual
  - book.snmp.md: SNMP
title: Клас SNMPException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SNMPException

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

## Вступ

Представляє клас виключення, що викидається SNMP. Ви не повинні викидати винятки **SNMPException** самостійно. Докладніше про винятки в PHP читайте у розділі [Винятки](language.exceptions.md)

## Огляд класів

```classsynopsis

     
      class SNMPException
     

     
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

## Властивості

code

Код ошибки библиотеки`SNMP`Для его извлечения используйте[Exception::getCode()](exception.getcode.md)
