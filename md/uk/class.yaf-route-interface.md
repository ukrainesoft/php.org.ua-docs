Клас YafRouteInterface

-   [« Yaf\_Response\_Abstract::\_\_toString](yaf-response-abstract.tostring.html)
    
-   [Yaf\_Route\_Interface::assemble »](yaf-route-interface.assemble.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRouteInterface
    

# Клас YafRouteInterface

(Yaf >=1.0.0)

## Вступ

**YafRouteInterface** використовується завдання власної маршрутизації.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Route_Interface
     
     {
    

    /* Методы */
    
   abstract public assemble(array $info, array $query = ?): string
abstract public route(Yaf_Request_Abstract $request): bool

   }
```

## Зміст

-   [Yaf\_Route\_Interface::assemble](yaf-route-interface.assemble.html) - Збирає запит
-   [Yaf\_Route\_Interface::route](yaf-route-interface.route.html) — Надсилання запиту