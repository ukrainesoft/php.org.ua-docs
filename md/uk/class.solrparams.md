Клас SolrParams

-   [« SolrGenericResponse::destruct](solrgenericresponse.destruct.html)
    
-   [SolrParams::add »](solrparams.add.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrParams
    

# Клас SolrParams

(PECL solr> = 0.9.2)

## Вступ

Представляє колекцію пар "ім'я-значення", що надсилається на сервер Solr під час запиту.

## Огляд класів

```classsynopsis



    
     
      abstract
      class SolrParams
     

     implements 
       Serializable {



    /* Методы */
    
   final public add(string $name, string $value): SolrParams
public addParam(string $name, string $value): SolrParams
final public get(string $param_name): mixed
final public getParam(string $param_name = ?): mixed
final public getParams(): array
final public getPreparedParams(): array
final public serialize(): string
final public set(string $name, string $value): void
public setParam(string $name, string $value): SolrParams
final public toString(bool $url_encode = false): string
final public unserialize(string $serialized): void

   }
```

## Зміст

-   [SolrParams::add](solrparams.add.html) - Псевдонім SolrParams::addParam
-   [SolrParams::addParam](solrparams.addparam.html) — Додає параметр до об'єкту
-   [SolrParams::get](solrparams.get.html) - Псевдонім SolrParams::getParam
-   [SolrParams::getParam](solrparams.getparam.html) — Повертає значення параметра
-   [SolrParams::getParams](solrparams.getparams.html) — Повертає масив параметрів, не в URL-закодованому вигляді
-   [SolrParams::getPreparedParams](solrparams.getpreparedparams.html) — Повертає масив параметрів в URL-адресі
-   [SolrParams::serialize](solrparams.serialize.html) — Використовується для серіалізації користувача
-   [SolrParams::set](solrparams.set.html) - Псевдонім SolrParams::setParam
-   [SolrParams::setParam](solrparams.setparam.html) — Встановлює параметр на вказане значення
-   [SolrParams::toString](solrparams.tostring.html) — Повертає всі параметри об'єкта у вигляді пар ім'я-значення
-   [SolrParams::unserialize](solrparams.unserialize.html) — Використовується для серіалізації користувача