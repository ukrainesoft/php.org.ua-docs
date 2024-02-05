---
navigation:
  - function.simdjson-key-value.md: « simdjson\_key\_value
  - class.simdjsonvalueerror.md: SimdJsonValueError »
  - index.md: PHP Manual
  - book.simdjson.md: Simdjson
title: Клас SimdJsonException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SimdJsonException

(PECL simdjson >= 2.1.0)

## Вступ

Виняток, що викидається функціями [simdjson\_decode()](function.simdjson-decode.md) [simdjson\_key\_count()](function.simdjson-key-count.md) [simdjson\_key\_exists()](function.simdjson-key-exists.md) або [simdjson\_key\_value()](function.simdjson-key-value.md). Можливі значення дивіться у константах [коди помилок simdjson](simdjson.constants.md)

## Огляд класів

```classsynopsis


    
    
     
      class SimdJsonException
     

     
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


   }
```
