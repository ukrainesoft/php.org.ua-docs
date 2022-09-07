---
navigation:
  - solrillegaloperationexception.getinternalinfo.md: '« SolrIllegalOperationException::getInternalInfo'
  - refs.utilspec.server.md: Модулі для роботи із серверами »
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrMissingMandatoryParameterException
---
# Клас SolrMissingMandatoryParameterException

(No version information available, might only be in Git)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class SolrMissingMandatoryParameterException
     

     
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
