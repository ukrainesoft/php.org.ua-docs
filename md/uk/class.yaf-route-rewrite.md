---
navigation:
  - yaf-route-regex.route.md: '« Yaf\_Route\_Regex::route'
  - yaf-route-rewrite.assemble.md: 'Yaf\_Route\_Rewrite::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Rewrite
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Rewrite

(Yaf >=1.0.0)

## Вступ

Приклад использования смотрите в разделе Прикладов[Yaf\_Route\_Rewrite::\_\_construct()](yaf-route-rewrite.construct.md)

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

\_route

\_default

\_verify

## Зміст

-   [Yaf\_Route\_Rewrite::assemble](yaf-route-rewrite.assemble.md) \- Збирає URL
-   [Yaf\_Route\_Rewrite::\_\_construct](yaf-route-rewrite.construct.md) \- Конструктор класу Yaf\_Route\_Rewrite
-   [Yaf\_Route\_Rewrite::route](yaf-route-rewrite.route.md) \- Призначення route
