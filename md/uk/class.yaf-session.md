Клас YafSession

-   [« Yaf\_Route\_Supervar::route](yaf-route-supervar.route.html)
    
-   [Yaf\_Session::\_\_construct »](yaf-session.construct.html)
    
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

-   [Yaf\_Session::\_\_construct](yaf-session.construct.html) - Конструктор класу YafSession
-   [Yaf\_Session::count](yaf-session.count.html) - Призначення count
-   [Yaf\_Session::current](yaf-session.current.html) - Призначення current
-   [Yaf\_Session::del](yaf-session.del.html) - Призначення del
-   [Yaf\_Session::\_\_get](yaf-session.get.html) - Призначення get
-   [Yaf\_Session::getInstance](yaf-session.getinstance.html) — Призначення getInstance
-   [Yaf\_Session::has](yaf-session.has.html) - Призначення has
-   [Yaf\_Session::\_\_isset](yaf-session.isset.html) - Призначення isset
-   [Yaf\_Session::key](yaf-session.key.html) - Призначення key
-   [Yaf\_Session::next](yaf-session.next.html) - Призначення next
-   [Yaf\_Session::offsetExists](yaf-session.offsetexists.html) — Призначення offsetExists
-   [Yaf\_Session::offsetGet](yaf-session.offsetget.html) - Призначення offsetGet
-   [Yaf\_Session::offsetSet](yaf-session.offsetset.html) - Призначення offsetSet
-   [Yaf\_Session::offsetUnset](yaf-session.offsetunset.html) - Призначення offsetUnset
-   [Yaf\_Session::rewind](yaf-session.rewind.html) - Призначення rewind
-   [Yaf\_Session::\_\_set](yaf-session.set.html) - Призначення set
-   [Yaf\_Session::start](yaf-session.start.html) - Призначення start
-   [Yaf\_Session::\_\_unset](yaf-session.unset.html) - Призначення unset
-   [Yaf\_Session::valid](yaf-session.valid.html) - Призначення valid