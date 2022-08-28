Клас YafRouteStatic

-   [« Yaf\_Route\_Simple::route](yaf-route-simple.route.html)
    
-   [Yaf\_Route\_Static::assemble »](yaf-route-static.assemble.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRouteStatic
    

# Клас YafRouteStatic

(Yaf >=1.0.0)

## Вступ

За замовчуванням, [Yaf\_Router](class.yaf-router.html) містить тільки **YafRouteStatic**

І **YafRouteStatic** спроектований таким чином, щоб покривати 80% усіх можливих потреб маршрутизації.

Будь ласка ЗВЕРНІТЬ УВАГУ, що не потрібно інстанціювати **YafRouteStatic**, також не потрібно додавати його до стек [Yaf\_Router](class.yaf-router.html), так як він є у стеку маршрутизації [Yaf\_Router](class.yaf-router.html) за замовчуванням і завжди буде викликатись останнім.

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

-   [Yaf\_Route\_Static::assemble](yaf-route-static.assemble.html) - Збирає URL
-   [Yaf\_Route\_Static::match](yaf-route-static.match.html) - Призначення match
-   [Yaf\_Route\_Static::route](yaf-route-static.route.html) — Надсилає запит