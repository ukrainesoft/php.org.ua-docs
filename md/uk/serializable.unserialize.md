Створює об'єкт

-   [« Serializable::serialize](serializable.serialize.html)
    
-   [Closure »](class.closure.html)
    
-   [PHP Manual](index.html)
    
-   [Serializable](class.serializable.html)
    
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
> Метод діє як [конструктор](language.oop5.decon.html#language.oop5.decon.constructor) об'єкт. Метод [\_\_construct()](language.oop5.decon.html#object.construct) *не* викликається після цього.

### Список параметрів

`data`

Строкове уявлення об'єкта.

### Значення, що повертаються

Значення методу, що повертається, ігнорується.

### Дивіться також

-   [\_\_wakeup()](language.oop5.magic.html#object.wakeup)
-   [\_\_unserialize()](language.oop5.magic.html#object.unserialize)