---
navigation:
  - solrclient.threads.md: '« SolrClient::threads'
  - solrresponse.getdigestedresponse.md: 'SolrResponse::getDigestedResponse »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrResponse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrResponse

(PECL solr >= 0.9.2)

## Вступ

Відповідь від сервера Solr.

## Огляд класів

```classsynopsis



    
     
      abstract
      class SolrResponse
     
     {

    /* Константы */
    
     const
     int
      PARSE_SOLR_OBJ = 0;

    const
     int
      PARSE_SOLR_DOC = 1;


    /* Свойства */
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
    
   public getDigestedResponse(): string
public getHttpStatus(): int
public getHttpStatusMessage(): string
public getRawRequest(): string
public getRawRequestHeaders(): string
public getRawResponse(): string
public getRawResponseHeaders(): string
public getRequestUrl(): string
public getResponse(): SolrObject
public setParseMode(int $parser_mode = 0): bool
public success(): bool

   }
```

## Властивості

http\_status

HTTP-статус відповіді.

parser\_mode

Чи слід аналізувати документи solr як екземпляри SolrObject чи SolrDocument.

success

Чи була помилка під час запиту

http\_status\_message

Детальне повідомлення про статус http

http\_request\_url

URL запиту

http\_raw\_request\_headers

Рядок необроблених заголовків, надісланих під час запиту.

http\_raw\_request

Необроблений запит, надісланий на сервер

http\_raw\_response\_headers

Заголовки відповіді сервера Solr.

http\_raw\_response

Повідомлення у відповідь від сервера.

http\_digested\_response

Відповідь у серіалізованому форматі PHP.

## Обумовлені константи

## Константи класу SolrResponse

**`SolrResponse::PARSE_SOLR_OBJ`**

Документи слід аналізувати як екземпляри SolrObject.

**`SolrResponse::PARSE_SOLR_DOC`**

Документи слід аналізувати як екземпляри SolrDocument.

## Зміст

-   [SolrResponse::getDigestedResponse](solrresponse.getdigestedresponse.md)— Повертає відповідь XML як серіалізовані дані PHP
-   [SolrResponse::getHttpStatus](solrresponse.gethttpstatus.md)— Повертає HTTP-статус відповіді
-   [SolrResponse::getHttpStatusMessage](solrresponse.gethttpstatusmessage.md)— Повертає докладнішу інформацію про статус HTTP
-   [SolrResponse::getRawRequest](solrresponse.getrawrequest.md)— Повертає необроблений запит, надісланий на сервер Solr
-   [SolrResponse::getRawRequestHeaders](solrresponse.getrawrequestheaders.md)— Повертає необроблені заголовки запиту на сервер Solr
-   [SolrResponse::getRawResponse](solrresponse.getrawresponse.md)— Повертає необроблену відповідь із сервера
-   [SolrResponse::getRawResponseHeaders](solrresponse.getrawresponseheaders.md)— Повертає необроблені заголовки відповіді із сервера
-   [SolrResponse::getRequestUrl](solrresponse.getrequesturl.md)— Повертає повну URL-адресу, на яку було надіслано запит.
-   [SolrResponse::getResponse](solrresponse.getresponse.md) \- Повертає SolrObject, що представляє відповідь XML від сервера
-   [SolrResponse::setParseMode](solrresponse.setparsemode.md)— Встановлює режим аналізу
-   [SolrResponse::success](solrresponse.success.md)— Чи був запит успішним?
