---
navigation:
  - yaf-dispatcher.throwexception.md: '« Yaf\_Dispatcher::throwException'
  - yaf-config-abstract.get.md: 'Yaf\_Config\_Abstract::get »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Config\_Abstract
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Config\_Abstract

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

\_config

\_readonly

## Зміст

-   [Yaf\_Config\_Abstract::get](yaf-config-abstract.get.md) \- Геттер
-   [Yaf\_Config\_Abstract::readonly](yaf-config-abstract.readonly.md)— Знаходить конфігурацію лише для читання
-   [Yaf\_Config\_Abstract::set](yaf-config-abstract.set.md) \- Сеттер
-   [Yaf\_Config\_Abstract::toArray](yaf-config-abstract.toarray.md) \- Приведення до масиву
