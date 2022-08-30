Клас YafConfigAbstract

-   [« YafDispatcher::throwException](yaf-dispatcher.throwexception.html)
    
-   [YafConfigAbstract::get »](yaf-config-abstract.get.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafConfigAbstract
    

# Клас YafConfigAbstract

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      abstract
      class Yaf_Config_Abstract
     
     {
    
    /* Свойства */
    
     protected
      $_config;

    protected
      $_readonly;



    /* Методы */
    
   abstract public get(string $name, mixed $value): mixed
abstract public readonly(): bool
abstract public set(): Yaf_Config_Abstract
abstract public toArray(): array

   }
```

## Властивості

config

readonly

## Зміст

-   [YafConfigAbstract::get](yaf-config-abstract.get.html) - Геттер
-   [YafConfigAbstract::readonly](yaf-config-abstract.readonly.html) — Знаходить конфігурацію лише для читання
-   [YafConfigAbstract::set](yaf-config-abstract.set.html) - Сеттер
-   [YafConfigAbstract::toArray](yaf-config-abstract.toarray.html) - Приведення до масиву