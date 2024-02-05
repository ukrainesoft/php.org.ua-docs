---
navigation:
  - soapparam.construct.md: '« SoapParam::\_\_construct'
  - soapvar.construct.md: 'SoapVar::\_\_construct »'
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: Клас SoapVar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SoapVar

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас, що представляє змінну або об'єкт для використання із сервісами SOAP.

## Огляд класів

```classsynopsis

    
     class SoapVar
     {

    /* Свойства */
    
     public
     int
      $enc_type;

    public
     mixed
      $enc_value = null;

    public
     ?string
      $enc_stype = null;

    public
     ?string
      $enc_ns = null;

    public
     ?string
      $enc_name = null;

    public
     ?string
      $enc_namens = null;


    /* Методы */
    
   public __construct(    mixed $data,    ?int $encoding,    ?string $typeName = null,    ?string $typeNamespace = null,    ?string $nodeName = null,    ?string $nodeNamespace = null)

   }
```

## Властивості

enc\_name

enc\_namens

enc\_ns

enc\_type

enc\_stype

enc\_value

## Зміст

-   [SoapVar::\_\_construct](soapvar.construct.md) \- Конструктор SoapVar
