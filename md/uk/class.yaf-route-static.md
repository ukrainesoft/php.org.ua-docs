---
navigation:
  - yaf-route-simple.route.md: '« Yaf\_Route\_Simple::route'
  - yaf-route-static.assemble.md: 'Yaf\_Route\_Static::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Static
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Static

(Yaf >=1.0.0)

## Вступ

По умолчанию,[Yaf\_Router](class.yaf-router.md) містить тільки **Yaf\_Route\_Static**

И**Yaf\_Route\_Static** спроектований таким чином, щоб покривати 80% усіх можливих потреб маршрутизації.

Пожалуйста\*ЗВЕРНІТЬ УВАГУ\*, що не потрібно інстанціювати **Yaf\_Route\_Static**, також не потрібно додавати його до стек [Yaf\_Router](class.yaf-router.md), так як він є у стеку маршрутизації [Yaf\_Router](class.yaf-router.md) за замовчуванням і завжди буде викликатись останнім.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Route_Static
     

     implements 
       Yaf_Router {
    

    /* Методы */
    
   public assemble(array $info, array $query = ?): string
public match(string $uri): void
public route(Yaf_Request_Abstract $request): bool

   }
```

## Зміст

-   [Yaf\_Route\_Static::assemble](yaf-route-static.assemble.md) \- Збирає URL
-   [Yaf\_Route\_Static::match](yaf-route-static.match.md) \- Призначення match
-   [Yaf\_Route\_Static::route](yaf-route-static.route.md)— Надсилає запит
