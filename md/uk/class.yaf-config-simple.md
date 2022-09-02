---
navigation:
  - yaf-config-ini.valid.md: '« YafConfigIni::valid'
  - yaf-config-simple.construct.md: 'YafConfigSimple::construct »'
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

-   [YafConfigSimple::construct](yaf-config-simple.construct.md) - Призначення construct
-   [YafConfigSimple::count](yaf-config-simple.count.md) - Призначення count
-   [YafConfigSimple::current](yaf-config-simple.current.md) - Призначення current
-   [YafConfigSimple::get](yaf-config-simple.get.md) - Призначення get
-   [YafConfigSimple::isset](yaf-config-simple.isset.md) - Призначення isset
-   [YafConfigSimple::key](yaf-config-simple.key.md) - Призначення key
-   [YafConfigSimple::next](yaf-config-simple.next.md) - Призначення next
-   [YafConfigSimple::offsetExists](yaf-config-simple.offsetexists.md) — Призначення offsetExists
-   [YafConfigSimple::offsetGet](yaf-config-simple.offsetget.md) - Призначення offsetGet
-   [YafConfigSimple::offsetSet](yaf-config-simple.offsetset.md) - Призначення offsetSet
-   [YafConfigSimple::offsetUnset](yaf-config-simple.offsetunset.md) - Призначення offsetUnset
-   [YafConfigSimple::readonly](yaf-config-simple.readonly.md) - Призначення readonly
-   [YafConfigSimple::rewind](yaf-config-simple.rewind.md) - Призначення rewind
-   [YafConfigSimple::set](yaf-config-simple.set.md) - Призначення set
-   [YafConfigSimple::toArray](yaf-config-simple.toarray.md) - Повертає масив PHP
-   [YafConfigSimple::valid](yaf-config-simple.valid.md) - Призначення valid
