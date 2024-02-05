---
navigation:
  - reserved.attributes.md: «Зумовлені атрибути
  - attribute.construct.md: 'Attribute::\_\_construct »'
  - index.md: PHP Manual
  - reserved.attributes.md: Зумовлені атрибути
title: Клас Attribute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Attribute

(PHP 8)

## Вступ

Атрибути дають можливість додавати структуровану, машиночитану інформацію метаданих про декларації в коді: метою атрибуту можуть бути класи, методи, функції, параметри, властивості та константи класу. Метадані, визначені атрибутами, можуть бути перевірені під час виконання за допомогою [Reflection API](book.reflection.md). Тому атрибути можна як мову конфігурації, вбудований у код.

## Огляд класів

```classsynopsis

    
     final
     class Attribute
     {

    /* Константы */
    
     const
     int
      TARGET_CLASS;

    const
     int
      TARGET_FUNCTION;

    const
     int
      TARGET_METHOD;

    const
     int
      TARGET_PROPERTY;

    const
     int
      TARGET_CLASS_CONSTANT;

    const
     int
      TARGET_PARAMETER;

    const
     int
      TARGET_ALL;

    const
     int
      IS_REPEATABLE;


    /* Свойства */
    public
     int
      $flags;


    /* Методы */
    
   public __construct(int $flags = Attribute::TARGET_ALL)

   }
```

## Обумовлені константи

**`Attribute::TARGET_CLASS`**

**`Attribute::TARGET_FUNCTION`**

**`Attribute::TARGET_METHOD`**

**`Attribute::TARGET_PROPERTY`**

**`Attribute::TARGET_CLASS_CONSTANT`**

**`Attribute::TARGET_PARAMETER`**

**`Attribute::TARGET_ALL`**

**`Attribute::IS_REPEATABLE`**

## Властивості

flags

## Дивіться також

[Введення в атрибути](language.attributes.md)

## Зміст

-   [Attribute::\_\_construct](attribute.construct.md) \- Створює новий екземпляр Attribute
