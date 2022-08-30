Клас SoapVar

-   [« SoapParam::construct](soapparam.construct.html)
    
-   [SoapVar::construct »](soapvar.construct.html)
    
-   [PHP Manual](index.html)
    
-   [SOAP](book.soap.html)
    
-   Клас SoapVar
    

# Клас SoapVar

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас, який представляє змінну чи об'єкт використання з сервісами SOAP.

## Огляд класів

```synopsis

     
    

    
     
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

encname

encnamens

encнс

enctype

encstype

encvalue

## Зміст

-   [SoapVar::construct](soapvar.construct.html) - Конструктор SoapVar