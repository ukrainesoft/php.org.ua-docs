Клас SNMPException

-   [« SNMP::walk](snmp.walk.html)
    
-   [Сокеты »](book.sockets.html)
    
-   [PHP Manual](index.html)
    
-   [SNMP](book.snmp.html)
    
-   Клас SNMPException
    

# Клас SNMPException

(PHP 5> = 5.4.0, PHP 7, PHP 8)

## Вступ

Представляє клас виключення SNMP, що викидається. Ви не повинні викидати винятки **SNMPException** самостійно. Докладніше про винятки в PHP читайте у розділі [Исключения](language.exceptions.html)

## Огляд класів

```classsynopsis

     
    

    
     
      class SNMPException
     

     
      extends
       RuntimeException
     
     {

    /* Свойства */
    
     protected
     string
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

Код помилки бібліотеки `SNMP`. Для його вилучення використовуйте [Exception::getCode()](exception.getcode.html)