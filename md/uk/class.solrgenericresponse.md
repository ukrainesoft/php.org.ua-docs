Клас SolrGenericResponse

-   [« SolrPingResponse::getResponse](solrpingresponse.getresponse.md)
    
-   [SolrGenericResponse::construct »](solrgenericresponse.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Solr](book.solr.md)
    
-   Клас SolrGenericResponse
    

# Клас SolrGenericResponse

(PECL solr> = 0.9.2)

## Вступ

Відповідь від сервера solr.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrGenericResponse
     

     
      extends
       SolrResponse
     
     {

    /* Константы */
    
     const
     int
      PARSE_SOLR_OBJ = 0;

    const
     int
      PARSE_SOLR_DOC = 1;


    /* Наследуемые свойства */
    const
     int
      SolrResponse::PARSE_SOLR_OBJ = 0;
const
     int
      SolrResponse::PARSE_SOLR_DOC = 1;
protected
     int
      $http_status;
protected
     int
      $parser_mode;
protected
     bool
      $success;
protected
     string
      $http_status_message;
protected
     string
      $http_request_url;
protected
     string
      $http_raw_request_headers;
protected
     string
      $http_raw_request;
protected
     string
      $http_raw_response_headers;
protected
     string
      $http_raw_response;
protected
     string
      $http_digested_response;


    /* Методы */
    
   public __construct()

    public __destruct()


    /* Наследуемые методы */
    public SolrResponse::getDigestedResponse(): string
public SolrResponse::getHttpStatus(): int
public SolrResponse::getHttpStatusMessage(): string
public SolrResponse::getRawRequest(): string
public SolrResponse::getRawRequestHeaders(): string
public SolrResponse::getRawResponse(): string
public SolrResponse::getRawResponseHeaders(): string
public SolrResponse::getRequestUrl(): string
public SolrResponse::getResponse(): SolrObject
public SolrResponse::setParseMode(int $parser_mode = 0): bool
public SolrResponse::success(): bool


   }
```

## Обумовлені константи

## Константи класу SolrGenericResponse

**`SolrGenericResponse::PARSE_SOLR_OBJ`**

Документи слід аналізувати як екземпляри SolrObject.

**`SolrGenericResponse::PARSE_SOLR_DOC`**

Документи слід аналізувати як екземпляри SolrDocument.

## Зміст

-   [SolrGenericResponse::construct](solrgenericresponse.construct.md) - Конструктор
-   [SolrGenericResponse::destruct](solrgenericresponse.destruct.md) - Деструктор