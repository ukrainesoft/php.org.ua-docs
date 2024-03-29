---
navigation:
  - solrillegalargumentexception.getinternalinfo.md: '« SolrIllegalArgumentException::getInternalInfo'
  - solrillegaloperationexception.getinternalinfo.md: 'SolrIllegalOperationException::getInternalInfo »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrIllegalOperationException
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrIllegalOperationException

(PECL solr >= 0.9.2)

## Вступ

Викидає, коли з об'єктом виконується неприпустима чи непідтримувана операція.

## Огляд класів

```classsynopsis


    
    
     
      class SolrIllegalOperationException
     

     
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

-   [SolrIllegalOperationException::getInternalInfo](solrillegaloperationexception.getinternalinfo.md)— Повертає внутрішню інформацію про те, де було викинуто виняток
