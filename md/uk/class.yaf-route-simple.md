---
navigation:
  - yaf-router.route.html: '« YafRouter::route'
  - yaf-route-simple.assemble.html: 'YafRouteSimple::assemble »'
  - index.html: PHP Manual
  - book.yaf.html: Yaf
title: Клас YafRouteSimple
---
# Клас YafRouteSimple

(Yaf >=1.0.0)

## Вступ

**YafRouteSimple** порівнюватиме рядок запиту та видаватиме інформацію за відповідним маршрутом.

Все, що вам потрібно зробити, це сказати **YafRouteSimple**який ключ в $GET є модулем, який контролером, а якою дією.

[YafRouteSimple::route()](yaf-route-simple.route.html) завжди повертає **`true`**, так що важливо помістити **YafRouteSimple** на початок стека маршрутизації, інакше ніяких інших маршрутизаторів не буде викликано.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Route_Simple
     

     implements 
       Yaf_Route_Interface {
    
    /* Свойства */
    
     protected
      $controller;

    protected
      $module;

    protected
      $action;



    /* Методы */
    
   public __construct(string $module_name, string $controller_name, string $action_name)

    public assemble(array $info, array $query = ?): string
public route(Yaf_Request_Abstract $request): bool

   }
```

## Властивості

controller

module

action

## Зміст

-   [YafRouteSimple::assemble](yaf-route-simple.assemble.html) - Збирає URL
-   [YafRouteSimple::construct](yaf-route-simple.construct.html) - Конструктор класу YafRouteSimple
-   [YafRouteSimple::route](yaf-route-simple.route.html) — Надсилає запит
