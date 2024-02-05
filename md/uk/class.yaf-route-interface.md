---
navigation:
  - yaf-response-abstract.tostring.md: '« Yaf\_Response\_Abstract::\_\_function toString() { [native code] }'
  - yaf-route-interface.assemble.md: 'Yaf\_Route\_Interface::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Interface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Interface

(Yaf >=1.0.0)

## Вступ

**Yaf\_Route\_Interface** використовується завдання власної маршрутизації.

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

-   [Yaf\_Route\_Interface::assemble](yaf-route-interface.assemble.md) \- Збирає запит
-   [Yaf\_Route\_Interface::route](yaf-route-interface.route.md)— Надсилання запиту
