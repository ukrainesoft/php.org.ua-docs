---
navigation:
  - yaf-route-map.route.md: '« Yaf\_Route\_Map::route'
  - yaf-route-regex.assemble.md: 'Yaf\_Route\_Regex::assemble »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Route\_Regex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Route\_Regex

(Yaf >=1.0.0)

## Вступ

**Yaf\_Route\_Regex** - Гнучкий маршрутизатор з усіх вбудованих маршрутизаторів Yaf.

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

\_route

\_default

\_maps

\_verify

## Зміст

-   [Yaf\_Route\_Regex::assemble](yaf-route-regex.assemble.md)— Сформувати URL-адресу
-   [Yaf\_Route\_Regex::\_\_construct](yaf-route-regex.construct.md) \- Конструктор класу Yaf\_Route\_Regex
-   [Yaf\_Route\_Regex::route](yaf-route-regex.route.md) \- Мета маршруту
