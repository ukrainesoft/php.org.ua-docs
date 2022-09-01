---
navigation:
  - yaf-config-ini.valid.html: '« YafConfigIni::valid'
  - yaf-config-simple.construct.html: 'YafConfigSimple::construct »'
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Клас YafConfigSimple
---
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

-   [YafConfigSimple::construct](yaf-config-simple.construct.html) - Призначення construct
-   [YafConfigSimple::count](yaf-config-simple.count.html) - Призначення count
-   [YafConfigSimple::current](yaf-config-simple.current.html) - Призначення current
-   [YafConfigSimple::get](yaf-config-simple.get.html) - Призначення get
-   [YafConfigSimple::isset](yaf-config-simple.isset.html) - Призначення isset
-   [YafConfigSimple::key](yaf-config-simple.key.html) - Призначення key
-   [YafConfigSimple::next](yaf-config-simple.next.html) - Призначення next
-   [YafConfigSimple::offsetExists](yaf-config-simple.offsetexists.html) — Призначення offsetExists
-   [YafConfigSimple::offsetGet](yaf-config-simple.offsetget.html) - Призначення offsetGet
-   [YafConfigSimple::offsetSet](yaf-config-simple.offsetset.html) - Призначення offsetSet
-   [YafConfigSimple::offsetUnset](yaf-config-simple.offsetunset.html) - Призначення offsetUnset
-   [YafConfigSimple::readonly](yaf-config-simple.readonly.html) - Призначення readonly
-   [YafConfigSimple::rewind](yaf-config-simple.rewind.html) - Призначення rewind
-   [YafConfigSimple::set](yaf-config-simple.set.html) - Призначення set
-   [YafConfigSimple::toArray](yaf-config-simple.toarray.html) - Повертає масив PHP
-   [YafConfigSimple::valid](yaf-config-simple.valid.html) - Призначення valid
