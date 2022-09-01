---
navigation:
  - yaf-response-abstract.tostring.html: '« YafResponseAbstract::toString'
  - yaf-route-interface.assemble.html: 'YafRouteInterface::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafRouteInterface
---
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

-   [YafRouteInterface::assemble](yaf-route-interface.assemble.md) - Збирає запит
-   [YafRouteInterface::route](yaf-route-interface.route.md) — Надсилання запиту
