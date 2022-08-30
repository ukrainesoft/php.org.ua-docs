Створює об'єкт

-   [« Serializable::serialize](serializable.serialize.md)
    
-   [Closure »](class.closure.md)
    
-   [PHP Manual](index.md)
    
-   [Serializable](class.serializable.md)
    
-   Створює об'єкт
    

# Serializable::unserialize

(PHP 5> = 5.1.0, PHP 7, PHP 8)

Serializable::unserialize — Створює об'єкт

### Опис

```methodsynopsis
public Serializable::unserialize(string $data): void
```

Викликається під час десеріалізації об'єкта.

> **Зауваження**
> 
> Метод діє як [конструктор](language.oop5.decon.html#language.oop5.decon.constructor) об'єкт. Метод [construct()](language.oop5.decon.html#object.construct) *не* викликається після цього.

### Список параметрів

`data`

Строкове уявлення об'єкта.

### Значення, що повертаються

Значення методу, що повертається, ігнорується.

### Дивіться також

-   [wakeup()](language.oop5.magic.html#object.wakeup)
-   [unserialize()](language.oop5.magic.html#object.unserialize)