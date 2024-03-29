---
navigation:
  - solrclientexception.getinternalinfo.md: '« SolrClientException::getInternalInfo'
  - solrserverexception.getinternalinfo.md: 'SolrServerException::getInternalInfo »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrServerException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrServerException

(PECL Solr >= 1.1.0, >=2.0.0)

## Вступ

Виняток, що виникає у разі виникнення помилки на сервері Solr.

## Огляд класів

```classsynopsis



    
     
      class SolrServerException
     

     
      extends
       SolrException
     
     {


    /* Наследуемые свойства */
    
      protected
      string
       $message = "";
private
      string
       $string = "";
protected
      int
       $code;
protected
      string
       $file = "";
protected
      int
       $line;
private
      array
       $trace = [];
private
      ?Throwable
       $previous = null;

    protected
     int
      $sourceline;
protected
     string
      $sourcefile;
protected
     string
      $zif_name;


    /* Методы */
    
   public getInternalInfo(): array


    /* Наследуемые методы */
    final public Exception::getMessage(): string
final public Exception::getPrevious(): ?Throwable
final public Exception::getCode(): int
final public Exception::getFile(): string
final public Exception::getLine(): int
final public Exception::getTrace(): array
final public Exception::getTraceAsString(): string
public Exception::__toString(): string
private Exception::__clone(): void

    public SolrException::getInternalInfo(): array


   }
```

## Зміст

-   [SolrServerException::getInternalInfo](solrserverexception.getinternalinfo.md)— Повертає внутрішню інформацію про те, де було викинуто виняток
