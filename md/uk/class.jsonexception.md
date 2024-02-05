---
navigation:
  - json.constants.md: « Зумовлені константи
  - class.jsonserializable.md: JsonSerializable »
  - index.md: PHP Manual
  - book.json.md: JSON
title: Клас JsonException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас JsonException

(PHP 7 >= 7.3.0, PHP 8)

## Вступ

Цей виняток викидається, якщо опція \*\*`JSON_THROW_ON_ERROR`\*\*установлена для функции[json\_encode()](function.json-encode.md) або [json\_decode()](function.json-decode.md). code містить тип помилки, дивіться можливі значення [json\_last\_error()](function.json-last-error.md)

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
