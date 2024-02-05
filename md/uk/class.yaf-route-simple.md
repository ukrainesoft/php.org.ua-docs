---
navigation:
  - yaf-router.route.md: '« Yaf\_Router::route'
  - yaf-route-simple.assemble.md: 'Yaf\_Route\_Simple::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Simple
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Simple

(Yaf >=1.0.0)

## Вступ

**Yaf\_Route\_Simple** порівнюватиме рядок запиту та видаватиме інформацію за відповідним маршрутом.

Все, що вам потрібно зробити, це сказати **Yaf\_Route\_Simple**який ключ в $\_GET є модулем, який контролером, а якою дією.

[Yaf\_Route\_Simple::route()](yaf-route-simple.route.md) завжди повертає **`true`**, так що важливо помістити **Yaf\_Route\_Simple** на початок стека маршрутизації, інакше ніяких інших маршрутизаторів не буде викликано.

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

-   [Yaf\_Route\_Simple::assemble](yaf-route-simple.assemble.md) \- Збирає URL
-   [Yaf\_Route\_Simple::\_\_construct](yaf-route-simple.construct.md) \- Конструктор класу Yaf\_Route\_Simple
-   [Yaf\_Route\_Simple::route](yaf-route-simple.route.md)— Надсилає запит
