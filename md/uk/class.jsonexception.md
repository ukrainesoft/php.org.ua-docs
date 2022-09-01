---
navigation:
  - json.constants.md: « Обумовлені константи
  - class.jsonserializable.md: JsonSerializable »
  - index.md: PHP Manual
  - book.json.md: JSON
title: Клас JsonException
---
# Клас JsonException

(PHP 7> = 7.3.0, PHP 8)

## Вступ

Цей виняток викидається, якщо опція **`JSON_THROW_ON_ERROR`** встановлена ​​для функції [jsonencode()](function.json-encode.html) або [jsondecode()](function.json-decode.html). code містить тип помилки, дивіться можливі значення [jsonlasterror()](function.json-last-error.md)

## Огляд класів

```classsynopsis

     
    

    
     
      class JsonException
     

     
      extends
       Exception
     
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
