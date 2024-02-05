---
navigation:
  - solrgenericresponse.destruct.md: '« SolrGenericResponse::\_\_destruct'
  - solrparams.add.md: 'SolrParams::add »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrParams
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrParams

(PECL solr >= 0.9.2)

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

-   [SolrParams::add](solrparams.add.md) \- Псевдонім SolrParams::addParam
-   [SolrParams::addParam](solrparams.addparam.md)— Додає параметр до об'єкту
-   [SolrParams::get](solrparams.get.md) \- Псевдонім SolrParams::getParam
-   [SolrParams::getParam](solrparams.getparam.md)— Повертає значення параметра
-   [SolrParams::getParams](solrparams.getparams.md)— Повертає масив параметрів, не в URL-закодованому вигляді
-   [SolrParams::getPreparedParams](solrparams.getpreparedparams.md)— Повертає масив параметрів в URL-адресі
-   [SolrParams::serialize](solrparams.serialize.md)— Використовується для серіалізації користувача
-   [SolrParams::set](solrparams.set.md) \- Псевдонім SolrParams::setParam
-   [SolrParams::setParam](solrparams.setparam.md)— Встановлює параметр на вказане значення
-   [SolrParams::toString](solrparams.tostring.md)— Повертає всі параметри об'єкта у вигляді пар ім'я-значення
-   [SolrParams::unserialize](solrparams.unserialize.md)— Використовується для серіалізації користувача
