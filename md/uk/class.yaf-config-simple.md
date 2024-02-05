---
navigation:
  - yaf-config-ini.valid.md: '« Yaf\_Config\_Ini::valid'
  - yaf-config-simple.construct.md: 'Yaf\_Config\_Simple::\_\_construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас Yaf\_Config\_Simple
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaf\_Config\_Simple

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

\_config

\_readonly

## Зміст

-   [Yaf\_Config\_Simple::\_\_construct](yaf-config-simple.construct.md) \- Призначення\_\_construct
-   [Yaf\_Config\_Simple::count](yaf-config-simple.count.md) \- Призначення count
-   [Yaf\_Config\_Simple::current](yaf-config-simple.current.md) \- Призначення current
-   [Yaf\_Config\_Simple::\_\_get](yaf-config-simple.get.md) \- Призначення\_\_get
-   [Yaf\_Config\_Simple::\_\_isset](yaf-config-simple.isset.md) \- Призначення\_\_isset
-   [Yaf\_Config\_Simple::key](yaf-config-simple.key.md) \- Призначення key
-   [Yaf\_Config\_Simple::next](yaf-config-simple.next.md) \- Призначення next
-   [Yaf\_Config\_Simple::offsetExists](yaf-config-simple.offsetexists.md)— Призначення offsetExists
-   [Yaf\_Config\_Simple::offsetGet](yaf-config-simple.offsetget.md) \- Призначення offsetGet
-   [Yaf\_Config\_Simple::offsetSet](yaf-config-simple.offsetset.md) \- Призначення offsetSet
-   [Yaf\_Config\_Simple::offsetUnset](yaf-config-simple.offsetunset.md) \- Призначення offsetUnset
-   [Yaf\_Config\_Simple::readonly](yaf-config-simple.readonly.md) \- Призначення readonly
-   [Yaf\_Config\_Simple::rewind](yaf-config-simple.rewind.md) \- Призначення rewind
-   [Yaf\_Config\_Simple::\_\_set](yaf-config-simple.set.md) \- Призначення\_\_set
-   [Yaf\_Config\_Simple::toArray](yaf-config-simple.toarray.md) \- Повертає масив PHP
-   [Yaf\_Config\_Simple::valid](yaf-config-simple.valid.md) \- Призначення valid
