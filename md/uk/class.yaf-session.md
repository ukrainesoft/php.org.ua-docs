Клас YafSession

-   [« YafRouteSupervar::route](yaf-route-supervar.route.html)
    
-   [YafSession::construct »](yaf-session.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafSession
    

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

-   [YafSession::construct](yaf-session.construct.html) - Конструктор класу YafSession
-   [YafSession::count](yaf-session.count.html) - Призначення count
-   [YafSession::current](yaf-session.current.html) - Призначення current
-   [YafSession::del](yaf-session.del.html) - Призначення del
-   [YafSession::get](yaf-session.get.html) - Призначення get
-   [YafSession::getInstance](yaf-session.getinstance.html) — Призначення getInstance
-   [YafSession::has](yaf-session.has.html) - Призначення has
-   [YafSession::isset](yaf-session.isset.html) - Призначення isset
-   [YafSession::key](yaf-session.key.html) - Призначення key
-   [YafSession::next](yaf-session.next.html) - Призначення next
-   [YafSession::offsetExists](yaf-session.offsetexists.html) — Призначення offsetExists
-   [YafSession::offsetGet](yaf-session.offsetget.html) - Призначення offsetGet
-   [YafSession::offsetSet](yaf-session.offsetset.html) - Призначення offsetSet
-   [YafSession::offsetUnset](yaf-session.offsetunset.html) - Призначення offsetUnset
-   [YafSession::rewind](yaf-session.rewind.html) - Призначення rewind
-   [YafSession::set](yaf-session.set.html) - Призначення set
-   [YafSession::start](yaf-session.start.html) - Призначення start
-   [YafSession::unset](yaf-session.unset.html) - Призначення unset
-   [YafSession::valid](yaf-session.valid.html) - Призначення valid