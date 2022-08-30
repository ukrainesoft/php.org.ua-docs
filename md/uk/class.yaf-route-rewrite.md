Клас YafRouteRewrite

-   [« YafRouteRegex::route](yaf-route-regex.route.html)
    
-   [YafRouteRewrite::assemble »](yaf-route-rewrite.assemble.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRouteRewrite
    

# Клас YafRouteRewrite

(Yaf >=1.0.0)

## Вступ

Приклад використання дивіться у розділі прикладів [YafRouteRewrite::construct()](yaf-route-rewrite.construct.html)

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Route_Rewrite
     

     
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
      $_verify;



    /* Методы */
    
   public __construct(string $match, array $route, array $verify = ?)

    public assemble(array $info, array $query = ?): string
public route(Yaf_Request_Abstract $request): bool


    /* Наследуемые методы */
    abstract public Yaf_Route_Interface::assemble(array $info, array $query = ?): string
abstract public Yaf_Route_Interface::route(Yaf_Request_Abstract $request): bool


   }
```

## Властивості

route

default

verify

## Зміст

-   [YafRouteRewrite::assemble](yaf-route-rewrite.assemble.html) - Збирає URL
-   [YafRouteRewrite::construct](yaf-route-rewrite.construct.html) - Конструктор класу YafRouteRewrite
-   [YafRouteRewrite::route](yaf-route-rewrite.route.html) - Призначення route