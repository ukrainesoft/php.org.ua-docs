Клас YafRouteRewrite

-   [« Yaf\_Route\_Regex::route](yaf-route-regex.route.html)
    
-   [Yaf\_Route\_Rewrite::assemble »](yaf-route-rewrite.assemble.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRouteRewrite
    

# Клас YafRouteRewrite

(Yaf >=1.0.0)

## Вступ

Приклад використання дивіться у розділі прикладів [Yaf\_Route\_Rewrite::\_\_construct()](yaf-route-rewrite.construct.html)

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

-   [Yaf\_Route\_Rewrite::assemble](yaf-route-rewrite.assemble.html) - Збирає URL
-   [Yaf\_Route\_Rewrite::\_\_construct](yaf-route-rewrite.construct.html) - Конструктор класу YafRouteRewrite
-   [Yaf\_Route\_Rewrite::route](yaf-route-rewrite.route.html) - Призначення route