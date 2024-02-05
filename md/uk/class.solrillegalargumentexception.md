---
navigation:
  - solrserverexception.getinternalinfo.md: '« SolrServerException::getInternalInfo'
  - solrillegalargumentexception.getinternalinfo.md: 'SolrIllegalArgumentException::getInternalInfo »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrIllegalArgumentException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrIllegalArgumentException

(PECL solr >= 0.9.2)

## Вступ

Викидається, коли методу передається неприпустимий чи некоректний аргумент.

## Огляд класів

```classsynopsis



    
     
      class SolrIllegalArgumentException
     

     
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

-   [SolrIllegalArgumentException::getInternalInfo](solrillegalargumentexception.getinternalinfo.md)— Повертає внутрішню інформацію про те, де було викинуто виняток
