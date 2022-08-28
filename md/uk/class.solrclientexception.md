Клас SolrClientException

-   [« SolrException::getInternalInfo](solrexception.getinternalinfo.html)
    
-   [SolrClientException::getInternalInfo »](solrclientexception.getinternalinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrClientException
    

# Клас SolrClientException

(PECL solr> = 0.9.2)

## Вступ

Виняток, що викидається у разі виникнення помилки під час запиту на сервер від клієнта.

## Огляд класів

```classsynopsis



    
     
      class SolrClientException
     

     
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

-   [SolrClientException::getInternalInfo](solrclientexception.getinternalinfo.html) — Повертає внутрішню інформацію про те, де було викинуто виняток