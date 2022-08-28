Клас YafConfigSimple

-   [« Yaf\_Config\_Ini::valid](yaf-config-ini.valid.html)
    
-   [Yaf\_Config\_Simple::\_\_construct »](yaf-config-simple.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafConfigSimple
    

# Клас YafConfigSimple

(Yaf >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Config_Simple
     

     
      extends
       Yaf_Config_Abstract
     

     implements 
       Iterator,  ArrayAccess,  Countable {
    
    /* Свойства */
    
     protected
      $_readonly;



    /* Методы */
    
   public __construct(array $configs, bool $readonly = false)

    public count(): void
public current(): void
public __get(string $name = ?): void
public __isset(string $name): void
public key(): void
public next(): void
public offsetExists(string $name): void
public offsetGet(string $name): void
public offsetSet(string $name, string $value): void
public offsetUnset(string $name): void
public readonly(): void
public rewind(): void
public __set(string $name, string $value): void
public toArray(): array
public valid(): void


    /* Наследуемые методы */
    abstract public Yaf_Config_Abstract::get(string $name, mixed $value): mixed
abstract public Yaf_Config_Abstract::readonly(): bool
abstract public Yaf_Config_Abstract::set(): Yaf_Config_Abstract
abstract public Yaf_Config_Abstract::toArray(): array


   }
```

## Властивості

config

readonly

## Зміст

-   [Yaf\_Config\_Simple::\_\_construct](yaf-config-simple.construct.html) - Призначення construct
-   [Yaf\_Config\_Simple::count](yaf-config-simple.count.html) - Призначення count
-   [Yaf\_Config\_Simple::current](yaf-config-simple.current.html) - Призначення current
-   [Yaf\_Config\_Simple::\_\_get](yaf-config-simple.get.html) - Призначення get
-   [Yaf\_Config\_Simple::\_\_isset](yaf-config-simple.isset.html) - Призначення isset
-   [Yaf\_Config\_Simple::key](yaf-config-simple.key.html) - Призначення key
-   [Yaf\_Config\_Simple::next](yaf-config-simple.next.html) - Призначення next
-   [Yaf\_Config\_Simple::offsetExists](yaf-config-simple.offsetexists.html) — Призначення offsetExists
-   [Yaf\_Config\_Simple::offsetGet](yaf-config-simple.offsetget.html) - Призначення offsetGet
-   [Yaf\_Config\_Simple::offsetSet](yaf-config-simple.offsetset.html) - Призначення offsetSet
-   [Yaf\_Config\_Simple::offsetUnset](yaf-config-simple.offsetunset.html) - Призначення offsetUnset
-   [Yaf\_Config\_Simple::readonly](yaf-config-simple.readonly.html) - Призначення readonly
-   [Yaf\_Config\_Simple::rewind](yaf-config-simple.rewind.html) - Призначення rewind
-   [Yaf\_Config\_Simple::\_\_set](yaf-config-simple.set.html) - Призначення set
-   [Yaf\_Config\_Simple::toArray](yaf-config-simple.toarray.html) - Повертає масив PHP
-   [Yaf\_Config\_Simple::valid](yaf-config-simple.valid.html) - Призначення valid