---
navigation:
  - yaf-route-supervar.route.md: '« YafRouteSupervar::route'
  - yaf-session.construct.md: 'YafSession::construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafSession
---
# Клас YafSession

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

instance

session

started

## Зміст

-   [YafSession::construct](yaf-session.construct.md) - Конструктор класу YafSession
-   [YafSession::count](yaf-session.count.md) - Призначення count
-   [YafSession::current](yaf-session.current.md) - Призначення current
-   [YafSession::del](yaf-session.del.md) - Призначення del
-   [YafSession::get](yaf-session.get.md) - Призначення get
-   [YafSession::getInstance](yaf-session.getinstance.md) — Призначення getInstance
-   [YafSession::has](yaf-session.has.md) - Призначення has
-   [YafSession::isset](yaf-session.isset.md) - Призначення isset
-   [YafSession::key](yaf-session.key.md) - Призначення key
-   [YafSession::next](yaf-session.next.md) - Призначення next
-   [YafSession::offsetExists](yaf-session.offsetexists.md) — Призначення offsetExists
-   [YafSession::offsetGet](yaf-session.offsetget.md) - Призначення offsetGet
-   [YafSession::offsetSet](yaf-session.offsetset.md) - Призначення offsetSet
-   [YafSession::offsetUnset](yaf-session.offsetunset.md) - Призначення offsetUnset
-   [YafSession::rewind](yaf-session.rewind.md) - Призначення rewind
-   [YafSession::set](yaf-session.set.md) - Призначення set
-   [YafSession::start](yaf-session.start.md) - Призначення start
-   [YafSession::unset](yaf-session.unset.md) - Призначення unset
-   [YafSession::valid](yaf-session.valid.md) - Призначення valid
