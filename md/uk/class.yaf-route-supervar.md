---
navigation:
  - yaf-route-static.route.md: '« Yaf\_Route\_Static::route'
  - yaf-route-supervar.assemble.md: 'Yaf\_Route\_Supervar::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Supervar
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Supervar

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

\_var\_name

## Зміст

-   [Yaf\_Route\_Supervar::assemble](yaf-route-supervar.assemble.md) \- Збирає URL
-   [Yaf\_Route\_Supervar::\_\_construct](yaf-route-supervar.construct.md) \- Призначення\_\_construct
-   [Yaf\_Route\_Supervar::route](yaf-route-supervar.route.md) \- Призначення route
