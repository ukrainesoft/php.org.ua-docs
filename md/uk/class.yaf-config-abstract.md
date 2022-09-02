---
navigation:
  - yaf-dispatcher.throwexception.md: '« YafDispatcher::throwException'
  - yaf-config-abstract.get.md: 'YafConfigAbstract::get »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafConfigAbstract
---
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

-   [YafConfigAbstract::get](yaf-config-abstract.get.md) - Геттер
-   [YafConfigAbstract::readonly](yaf-config-abstract.readonly.md) — Знаходить конфігурацію лише для читання
-   [YafConfigAbstract::set](yaf-config-abstract.set.md) - Сеттер
-   [YafConfigAbstract::toArray](yaf-config-abstract.toarray.md) - Приведення до масиву
