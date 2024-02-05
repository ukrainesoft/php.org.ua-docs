---
navigation:
  - solrparams.unserialize.md: '« SolrParams::unserialize'
  - solrmodifiableparams.construct.md: 'SolrModifiableParams::\_\_construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrModifiableParams
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrModifiableParams

(PECL solr >= 0.9.2)

## Вступ

Представляє колекцію пар "ім'я-значення", що надсилається на сервер Solr під час запиту.

## Огляд класів

```classsynopsis



    
     
      class SolrModifiableParams
     

     
      extends
       SolrParams
     

     implements 
       Serializable {


    /* Методы */
    
   public __construct()

    public __destruct()


    /* Наследуемые методы */
    final public SolrParams::add(string $name, string $value): SolrParams
public SolrParams::addParam(string $name, string $value): SolrParams
final public SolrParams::get(string $param_name): mixed
final public SolrParams::getParam(string $param_name = ?): mixed
final public SolrParams::getParams(): array
final public SolrParams::getPreparedParams(): array
final public SolrParams::serialize(): string
final public SolrParams::set(string $name, string $value): void
public SolrParams::setParam(string $name, string $value): SolrParams
final public SolrParams::toString(bool $url_encode = false): string
final public SolrParams::unserialize(string $serialized): void


   }
```

## Зміст

-   [SolrModifiableParams::\_\_construct](solrmodifiableparams.construct.md) \- Конструктор
-   [SolrModifiableParams::\_\_destruct](solrmodifiableparams.destruct.md) \- Деструктор
