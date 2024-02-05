---
navigation:
  - class.simdjsonexception.md: « SimdJsonException
  - book.lua.md: Lua »
  - index.md: PHP Manual
  - book.simdjson.md: Simdjson
title: Клас SimdJsonValueError
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SimdJsonValueError

(PECL simdjson >= 3.0.0)

## Вступ

Ошибка**SimdJsonValueError** викидається, коли тип аргументу функції simdjson є правильним, але його значення неправильне. Наприклад, коли JSON-декодоване значення $depth не є позитивним або значення $depth занадто велике.

## Огляд класів

```classsynopsis


    
    
     
      class SimdJsonValueError
     

     
      extends
       ValueError
     
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
    
   final public Error::getMessage(): string
final public Error::getPrevious(): ?Throwable
final public Error::getCode(): int
final public Error::getFile(): string
final public Error::getLine(): int
final public Error::getTrace(): array
final public Error::getTraceAsString(): string
public Error::__toString(): string
private Error::__clone(): void


   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PHP 8.0.0 | Класс**SimdJsonValueError** тепер розширює [ValueError](class.valueerror.md) замість [Error](class.error.md) |
