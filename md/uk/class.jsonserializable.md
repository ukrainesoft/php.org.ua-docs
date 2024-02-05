---
navigation:
  - class.jsonexception.md: « JsonException
  - jsonserializable.jsonserialize.md: 'JsonSerializable::jsonSerialize »'
  - index.md: PHP Manual
  - book.json.md: JSON
title: Інтерфейс JsonSerializable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс JsonSerializable

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

## Вступ

Об'єкти, що реалізують інтерфейс **JsonSerializable**, можуть модифікувати своє JSON-подання при кодуванні за допомогою [json\_encode()](function.json-encode.md)

## Огляд інтерфейсів

```classsynopsis

    
     interface JsonSerializable {

    /* Методы */
    
   public jsonSerialize(): mixed

   }
```

## Зміст

-   [JsonSerializable::jsonSerialize](jsonserializable.jsonserialize.md)— Задає дані, які мають бути серіалізовані у JSON
