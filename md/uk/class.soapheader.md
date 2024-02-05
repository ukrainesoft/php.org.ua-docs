---
navigation:
  - soapfault.tostring.md: '« SoapFault::\_\_function toString() { [native code] }'
  - soapheader.construct.md: 'SoapHeader::\_\_construct »'
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: Клас SoapHeader
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SoapHeader

(PHP 5, PHP 7, PHP 8)

## Вступ

Заголовок SOAP.

## Огляд класів

```classsynopsis

    
     class SoapHeader
     {

    /* Свойства */
    
     public
     string
      $namespace;

    public
     string
      $name;

    public
     mixed
      $data = null;

    public
     bool
      $mustUnderstand;

    public
     string|int|null
      $actor;


    /* Методы */
    
   public __construct(    string $namespace,    string $name,    mixed $data = ?,    bool $mustunderstand = ?,    string $actor = ?)

   }
```

## Властивості

actor

data

mustUnderstand

name

namespace

## Зміст

-   [SoapHeader::\_\_construct](soapheader.construct.md) \- Конструктор SoapHeader
