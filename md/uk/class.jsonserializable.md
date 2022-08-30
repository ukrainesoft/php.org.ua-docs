Інтерфейс JsonSerializable

-   [« JsonException](class.jsonexception.html)
    
-   [JsonSerializable::jsonSerialize »](jsonserializable.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [JSON](book.json.html)
    
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

-   [JsonSerializable::jsonSerialize](jsonserializable.jsonserialize.html) — Задає дані, які мають бути серіалізовані у JSON