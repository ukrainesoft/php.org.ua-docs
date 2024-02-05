---
navigation:
  - backedenum.tryfrom.md: '« BackedEnum::tryFrom'
  - sensitiveparametervalue.construct.md: 'SensitiveParameterValue::\_\_construct »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас SensitiveParameterValue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SensitiveParameterValue

(PHP 8 >= 8.2.0)

## Вступ

Класс**SensitiveParameterValue** дозволяє обернути чутливі значення, щоб захистити їх від випадкового розкриття.

Значення параметрів з атрибутом [SensitiveParameter](class.sensitiveparameter.md) будуть автоматично обгорнуті всередині об'єкту **SensitiveParameterValue** у трасуваннях стека.

## Огляд класів

```classsynopsis

    
     final
     class SensitiveParameterValue
     {

    /* Свойства */
    
     private
     readonly
     mixed
      $value;


    /* Методы */
    
   public __construct(mixed $value)

    public __debugInfo(): array
public getValue(): mixed

   }
```

## Властивості

value

Чутливе значення, яке потрібно захистити від випадкового впливу.

## Зміст

-   [SensitiveParameterValue::\_\_construct](sensitiveparametervalue.construct.md)— Створює новий об'єкт Sensitive Parameter Value
-   [SensitiveParameterValue::\_\_debugInfo](sensitiveparametervalue.debuginfo.md)— Захист чутливих значень від випадкової дії
-   [SensitiveParameterValue::getValue](sensitiveparametervalue.getvalue.md)— Повертає чутливе значення
