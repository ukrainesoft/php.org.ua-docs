---
navigation:
  - override.construct.md: '« Override::\_\_construct'
  - returntypewillchange.construct.md: 'ReturnTypeWillChange::\_\_construct »'
  - index.md: PHP Manual
  - reserved.attributes.md: Зумовлені атрибути
title: Клас ReturnTypeWillChange
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReturnTypeWillChange

(PHP 8 >= 8.1.0)

## Вступ

Більшість неостаточних внутрішніх методів тепер вимагають, щоб перевизначальні методи оголошували сумісний тип значення, що повертається, інакше при перевірці успадкування буде видано повідомлення про старіння. Якщо тип повертаного значення не може бути оголошений для перевизначуваного методу через проблеми сумісності з крос-версіями PHP, може бути доданий атрибут `#[\ReturnTypeWillChange]`, щоб заглушити повідомлення про старіння.

## Огляд класів

```classsynopsis

    
     final
     class ReturnTypeWillChange
     {

    /* Методы */
    
   public __construct()

   }
```

## Дивіться також

[Введення в атрибути](language.attributes.md)

## Зміст

-   [ReturnTypeWillChange::\_\_construct](returntypewillchange.construct.md)— Створює новий екземпляр атрибуту ReturnTypeWillChange
