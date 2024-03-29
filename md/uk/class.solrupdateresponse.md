---
navigation:
  - solrqueryresponse.destruct.md: '« SolrQueryResponse::\_\_destruct'
  - solrupdateresponse.construct.md: 'SolrUpdateResponse::\_\_construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrUpdateResponse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrUpdateResponse

(PECL solr >= 0.9.2)

## Вступ

Відповідь на запит на оновлення.

## Огляд класів

```classsynopsis



    
     
      final
      class SolrUpdateResponse
     

     
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

## Константи класу SolrUpdateResponse

**`SolrUpdateResponse::PARSE_SOLR_OBJ`**

Документи слід аналізувати як екземпляри SolrObject

**`SolrUpdateResponse::PARSE_SOLR_DOC`**

Документи слід аналізувати як екземпляри SolrDocument

## Зміст

-   [SolrUpdateResponse::\_\_construct](solrupdateresponse.construct.md) \- Конструктор
-   [SolrUpdateResponse::\_\_destruct](solrupdateresponse.destruct.md) \- Деструктор
