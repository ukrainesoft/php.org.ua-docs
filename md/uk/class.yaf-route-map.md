---
navigation:
  - yaf-route-interface.route.md: '« Yaf\_Route\_Interface::route'
  - yaf-route-map.assemble.md: 'Yaf\_Route\_Map::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Map
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Map

(Yaf >=1.0.0)

## Вступ

**Yaf\_Route\_Map** — це вбудований маршрут, він просто перетворює кінцеву точку URI (ту частину URI, яка йде після базового URI: дивіться опис методу [Yaf\_Request\_Abstract::setBaseUri()](yaf-request-abstract.setbaseuri.md)) в ім'я контролера або ім'я дії (залежить від параметра, переданого в метод [Yaf\_Route\_Map::\_\_construct()](yaf-route-map.construct.md)) у наступному правилі: A => controller A. A/B/C => controller A\_B\_C. A/B/C/D/E => controller A\_B\_C\_D\_E.

If the second parameter of[Yaf\_Route\_Map::\_\_construct()](yaf-route-map.construct.md)is specified, then only the part before delimiter of URI will used to routing, the part after it is used to routing request parameters (see the example section of[Yaf\_Route\_Map::\_\_construct()](yaf-route-map.construct.md)

## Огляд класів

```classsynopsis



    
     
      class Yaf_Route_Map
     

     implements 
       Yaf_Route_Interface {

    /* Свойства */
    
     protected
      $_ctl_router;

    protected
      $_delimiter;



    /* Методы */
    
   public __construct(string $controller_prefer = false, string $delimiter = "")

    public assemble(array $info, array $query = ?): string
public route(Yaf_Request_Abstract $request): bool

   }
```

## Властивості

\_ctl\_router

\_delimiter

## Зміст

-   [Yaf\_Route\_Map::assemble](yaf-route-map.assemble.md) \- Збирає URL
-   [Yaf\_Route\_Map::\_\_construct](yaf-route-map.construct.md) \- Призначення\_\_construct
-   [Yaf\_Route\_Map::route](yaf-route-map.route.md) \- Призначення route
