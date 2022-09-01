---
navigation:
  - yaf-route-static.route.html: '« YafRouteStatic::route'
  - yaf-route-supervar.assemble.html: 'YafRouteSupervar::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafRouteSupervar
---
# Клас YafRouteSupervar

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Route_Supervar
     

     implements 
       Yaf_Route_Interface {
    
    /* Свойства */
    
     protected
      $_var_name;



    /* Методы */
    
   public __construct(string $supervar_name)

    public assemble(array $info, array $query = ?): string
public route(Yaf_Request_Abstract $request): bool

   }
```

## Властивості

varname

## Зміст

-   [YafRouteSupervar::assemble](yaf-route-supervar.assemble.html) - Збирає URL
-   [YafRouteSupervar::construct](yaf-route-supervar.construct.html) - Призначення construct
-   [YafRouteSupervar::route](yaf-route-supervar.route.html) - Призначення route
