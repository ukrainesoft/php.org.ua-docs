---
navigation:
  - soapserver.setpersistence.md: '« SoapServer::setPersistence'
  - soapfault.construct.md: 'SoapFault::\_\_construct »'
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: Клас SoapFault
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SoapFault

(PHP 5, PHP 7, PHP 8)

## Вступ

Помилка SOAP.

## Огляд класів

```classsynopsis

    
     class SoapFault
    

    
     extends
      Exception
     {

    /* Свойства */
    
     public
     string
      $faultstring;

    public
     ?string
      $faultcode = null;

    public
     ?string
      $faultcodens = null;

    public
     ?string
      $faultactor = null;

    public
     mixed
      $detail = null;

    public
     ?string
      $_name = null;

    public
     mixed
      $headerfault = null;


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


    /* Методы */
    
   public __construct(    array|string|null $code,    string $string,    ?string $actor = null,    mixed $details = null,    ?string $name = null,    mixed $headerFault = null)

    public __toString(): string


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

\_name

detail

faultactor

faultcode

faultcodens

faultstring

headerfault

## Зміст

-   [SoapFault::\_\_construct](soapfault.construct.md) \- Конструктор SoapFault
-   [SoapFault::\_\_function toString() { \[native code\] }](soapfault.tostring.md)— Отримати текстове уявлення SoapFault
