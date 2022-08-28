Клас SolrException

-   [« SolrCollapseFunction::\_\_toString](solrcollapsefunction.tostring.html)
    
-   [SolrException::getInternalInfo »](solrexception.getinternalinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrException
    

# Клас SolrException

(PECL solr> = 0.9.2)

## Вступ

Базовий клас для всіх винятків, які викидають класи модуля Solr.

## Огляд класів

```classsynopsis



    
     
      class SolrException
     

     
      extends
       Exception
     
     {

    /* Свойства */
    
     protected
     int
      $sourceline;

    protected
     string
      $sourcefile;

    protected
     string
      $zif_name;


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


   }
```

## Властивості

sourceline

Рядок у вихідному файлі c-space, де було згенеровано виняток

sourcefile

Вихідний файл c-space, де було згенеровано виняток

zifname

Функція c-space, де було згенеровано виняток

## Зміст

-   [SolrException::getInternalInfo](solrexception.getinternalinfo.html) — Повертає внутрішню інформацію про те, де було викинуто виняток