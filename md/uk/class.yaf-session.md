---
navigation:
  - yaf-route-supervar.route.md: '« Yaf\_Route\_Supervar::route'
  - yaf-session.construct.md: 'Yaf\_Session::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Session
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Session

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Session
     

     implements 
       Iterator,  ArrayAccess,  Countable {
    
    /* Свойства */
    
     protected
     static
      $_instance;

    protected
      $_session;

    protected
      $_started;



    /* Методы */
    
   private __construct()

    public count(): void
public current(): void
public del(string $name): void
public __get(string $name): void
public static getInstance(): void
public has(string $name): void
public __isset(string $name): void
public key(): void
public next(): void
public offsetExists(string $name): void
public offsetGet(string $name): void
public offsetSet(string $name, string $value): void
public offsetUnset(string $name): void
public rewind(): void
public __set(string $name, string $value): void
public start(): void
public __unset(string $name): void
public valid(): void

   }
```

## Властивості

\_instance

\_session

\_started

## Зміст

-   [Yaf\_Session::\_\_construct](yaf-session.construct.md) \- Конструктор класу Yaf\_Session
-   [Yaf\_Session::count](yaf-session.count.md) \- Призначення count
-   [Yaf\_Session::current](yaf-session.current.md) \- Призначення current
-   [Yaf\_Session::del](yaf-session.del.md) \- Призначення del
-   [Yaf\_Session::\_\_get](yaf-session.get.md) \- Призначення\_\_get
-   [Yaf\_Session::getInstance](yaf-session.getinstance.md)— Призначення getInstance
-   [Yaf\_Session::has](yaf-session.has.md) \- Призначення has
-   [Yaf\_Session::\_\_isset](yaf-session.isset.md) \- Призначення\_\_isset
-   [Yaf\_Session::key](yaf-session.key.md) \- Призначення key
-   [Yaf\_Session::next](yaf-session.next.md) \- Призначення next
-   [Yaf\_Session::offsetExists](yaf-session.offsetexists.md)— Призначення offsetExists
-   [Yaf\_Session::offsetGet](yaf-session.offsetget.md) \- Призначення offsetGet
-   [Yaf\_Session::offsetSet](yaf-session.offsetset.md) \- Призначення offsetSet
-   [Yaf\_Session::offsetUnset](yaf-session.offsetunset.md) \- Призначення offsetUnset
-   [Yaf\_Session::rewind](yaf-session.rewind.md) \- Призначення rewind
-   [Yaf\_Session::\_\_set](yaf-session.set.md) \- Призначення\_\_set
-   [Yaf\_Session::start](yaf-session.start.md) \- Призначення start
-   [Yaf\_Session::\_\_unset](yaf-session.unset.md) \- Призначення\_\_unset
-   [Yaf\_Session::valid](yaf-session.valid.md) \- Призначення valid
