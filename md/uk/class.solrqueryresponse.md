Клас SolrQueryResponse

-   [« SolrResponse::success](solrresponse.success.html)
    
-   [SolrQueryResponse::\_\_construct »](solrqueryresponse.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrQueryResponse
    

# Клас SolrQueryResponse

(PECL solr> = 0.9.2)

## Вступ

Відповідь на запит запиту.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrQueryResponse
     

     
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

## Константи класу SolrResponse

**`SolrQueryResponse::PARSE_SOLR_OBJ`**

Документи слід аналізувати як екземпляри SolrObject.

**`SolrQueryResponse::PARSE_SOLR_DOC`**

Документи слід аналізувати як екземпляри SolrDocument.

## Зміст

-   [SolrQueryResponse::\_\_construct](solrqueryresponse.construct.html) - Конструктор
-   [SolrQueryResponse::\_\_destruct](solrqueryresponse.destruct.html) - Деструктор