---
navigation:
  - soapfault.tostring.md: '« SoapFault::toString'
  - soapheader.construct.md: 'SoapHeader::construct »'
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: Клас SoapHeader
---
# Клас SoapHeader

(PHP 5, PHP 7, PHP 8)

## Вступ

Заголовок SOAP.

## Огляд класів

```synopsis

     
    

    
     
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
    
   __construct(    string $namespace,    string $name,    mixed $data = ?,    bool $mustunderstand = ?,    string $actor = ?)

   }
```

## Властивості

actor

data

mustUnderstand

name

namespace

## Зміст

-   [SoapHeader::construct](soapheader.construct.md) - Конструктор SoapHeader
