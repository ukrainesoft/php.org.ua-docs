Клас YafRouteMap

-   [« YafRouteInterface::route](yaf-route-interface.route.html)
    
-   [YafRouteMap::assemble »](yaf-route-map.assemble.html)
    
-   [PHP Manual](index.md)
    
-   [Yaf](book.yaf.md)
    
-   Клас YafRouteMap
    

# Клас YafRouteMap

(Yaf >=1.0.0)

## Вступ

**YafRouteMap** - це вбудований маршрут, він просто перетворює кінцеву точку URI (ту частину URI, яка йде після базового URI: дивіться [YafRequestAbstract::setBaseUri()](yaf-request-abstract.setbaseuri.html)) в ім'я контролера або ім'я дії (залежить від параметра, переданого в [YafRouteMap::construct()](yaf-route-map.construct.html)) у наступному правилі: A => controller A. A/B/C => controller AУC. A/B/C/D/E => controller AУЗДе.

If the second parameter of [YafRouteMap::construct()](yaf-route-map.construct.html) is specified, then only the part before delimiter of URI will used to routing, the part after it is used to routing request parameters (see the example section of [YafRouteMap::construct()](yaf-route-map.construct.html)

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

ctlrouter

delimiter

## Зміст

-   [YafRouteMap::assemble](yaf-route-map.assemble.html) - Збирає URL
-   [YafRouteMap::construct](yaf-route-map.construct.html) - Призначення construct
-   [YafRouteMap::route](yaf-route-map.route.html) - Призначення route