Клас SolrModifiableParams

-   [« SolrParams::unserialize](solrparams.unserialize.html)
    
-   [SolrModifiableParams::construct »](solrmodifiableparams.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrModifiableParams
    

# Клас SolrModifiableParams

(PECL solr> = 0.9.2)

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

-   [SolrModifiableParams::construct](solrmodifiableparams.construct.html) - Конструктор
-   [SolrModifiableParams::destruct](solrmodifiableparams.destruct.html) - Деструктор