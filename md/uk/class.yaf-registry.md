---
navigation:
  - yaf-plugin-abstract.routerstartup.md: '« Yaf\_Plugin\_Abstract::routerStartup'
  - yaf-registry.construct.md: 'Yaf\_Registry::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Registry
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Registry

(Yaf >=1.0.0)

## Вступ

Усі методи **Yaf\_Registry** визначено як статичні, роблячи їх універсально доступними. Це надає можливості прочитати або записати будь-які дані з будь-якого місця у вашому додатку.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Registry
     
     {
    
    /* Свойства */
    
     static
      $_instance;

    protected
      $_entries;



    /* Методы */
    
   private __construct()

    public static del(string $name): void
public static get(string $name): mixed
public static has(string $name): bool
public static set(string $name, string $value): bool

   }
```

## Властивості

\_instance

\_entries

## Зміст

-   [Yaf\_Registry::\_\_construct](yaf-registry.construct.md)— Yaf\_Registry реалізує шаблон проектування "Одиночка"
-   [Yaf\_Registry::del](yaf-registry.del.md)— Видаляє елемент із реєстру
-   [Yaf\_Registry::get](yaf-registry.get.md)— Отримує елемент із реєстру
-   [Yaf\_Registry::has](yaf-registry.has.md)— Перевіряє, чи існує елемент
-   [Yaf\_Registry::set](yaf-registry.set.md)— Додає елемент до реєстру
