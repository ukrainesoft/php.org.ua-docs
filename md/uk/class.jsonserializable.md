Інтерфейс JsonSerializable

-   [« JsonException](class.jsonexception.md)
    
-   [JsonSerializable::jsonSerialize »](jsonserializable.jsonserialize.md)
    
-   [PHP Manual](index.md)
    
-   [JSON](book.json.md)
    
-   Інтерфейс JsonSerializable
    

# Інтерфейс JsonSerializable

(PHP 5> = 5.4.0, PHP 7, PHP 8)

## Вступ

Об'єкти, що реалізують інтерфейс **JsonSerializable**, можуть модифікувати своє JSON-подання при кодуванні за допомогою [jsonencode()](function.json-encode.html)

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface JsonSerializable {

    /* Методы */
    
   public jsonSerialize(): mixed

   }
```

## Зміст

-   [JsonSerializable::jsonSerialize](jsonserializable.jsonserialize.md) — Задає дані, які мають бути серіалізовані у JSON