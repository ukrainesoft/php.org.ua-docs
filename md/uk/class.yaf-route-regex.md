Клас YafRouteRegex

-   [« YafRouteMap::route](yaf-route-map.route.html)
    
-   [YafRouteRegex::assemble »](yaf-route-regex.assemble.html)
    
-   [PHP Manual](index.md)
    
-   [Yaf](book.yaf.md)
    
-   Клас YafRouteRegex
    

# Клас YafRouteRegex

(Yaf >=1.0.0)

## Вступ

**YafRouteRegex** - Гнучкий маршрутизатор з усіх вбудованих маршрутизаторів Yaf.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Route_Regex
     

     
      extends
       Yaf_Route_Interface
     

     implements 
       Yaf_Route_Interface {
    
    /* Свойства */
    
     protected
      $_route;

    protected
      $_default;

    protected
      $_maps;

    protected
      $_verify;



    /* Методы */
    
   public __construct(    string $match,    array $route,    array $map = ?,    array $verify = ?,    string $reverse = ?)

    public assemble(array $info, array $query = ?): ?string
public route(Yaf_Request_Abstract $request): bool


    /* Наследуемые методы */
    abstract public Yaf_Route_Interface::assemble(array $info, array $query = ?): string
abstract public Yaf_Route_Interface::route(Yaf_Request_Abstract $request): bool


   }
```

## Властивості

route

default

maps

verify

## Зміст

-   [YafRouteRegex::assemble](yaf-route-regex.assemble.html) — Сформувати URL-адресу
-   [YafRouteRegex::construct](yaf-route-regex.construct.html) - Конструктор класу YafRouteRegex
-   [YafRouteRegex::route](yaf-route-regex.route.html) - Мета маршруту