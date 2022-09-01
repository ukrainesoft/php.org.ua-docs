---
navigation:
  - yaf-route-simple.route.html: '« YafRouteSimple::route'
  - yaf-route-static.assemble.html: 'YafRouteStatic::assemble »'
  - index.html: PHP Manual
  - book.yaf.html: Yaf
title: Клас YafRouteStatic
---
# Клас YafRouteStatic

(Yaf >=1.0.0)

## Вступ

За замовчуванням, [YafRouter](class.yaf-router.md) містить тільки **YafRouteStatic**

І **YafRouteStatic** спроектований таким чином, щоб покривати 80% усіх можливих потреб маршрутизації.

Будь ласка ЗВЕРНІТЬ УВАГУ, що не потрібно інстанціювати **YafRouteStatic**, також не потрібно додавати його до стек [YafRouter](class.yaf-router.html), так як він є у стеку маршрутизації [YafRouter](class.yaf-router.md) за замовчуванням і завжди буде викликатись останнім.

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

-   [YafRouteStatic::assemble](yaf-route-static.assemble.md) - Збирає URL
-   [YafRouteStatic::match](yaf-route-static.match.md) - Призначення match
-   [YafRouteStatic::route](yaf-route-static.route.md) — Надсилає запит
