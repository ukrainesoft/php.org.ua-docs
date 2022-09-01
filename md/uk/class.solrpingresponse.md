---
navigation:
  - solrupdateresponse.destruct.md: '« SolrUpdateResponse::destruct'
  - solrpingresponse.construct.md: 'SolrPingResponse::construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrPingResponse
---
# Клас SolrPingResponse

(PECL solr> = 0.9.2)

## Вступ

Відповідь на запит ping до сервера

## Огляд класів

```classsynopsis



    
     
      final
      class SolrPingResponse
     

     
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


    /* Свойства */


    /* Методы */
    
   public __construct()

    public getResponse(): string

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

## Властивості

httpstatus

HTTP-статус відповіді.

parsermode

Чи слід аналізувати документи solr як екземпляри SolrObject чи SolrDocument.

success

Чи була помилка під час запиту

httpstatusmessage

Детальне повідомлення про статус http

httprequesturl

URL запиту

httprawrequestheaders

Рядок необроблених заголовків, надісланих під час запиту

httprawrequest

Необроблений запит, надісланий на сервер

httprawresponseheaders

Заголовки відповіді від сервера Solr

httprawresponse

Повідомлення у відповідь від сервера

httpdigestedresponse

Відповідь у серіалізованому форматі PHP.

## Обумовлені константи

## Константи класу SolrPingResponse

**`SolrPingResponse::PARSE_SOLR_OBJ`**

Документи слід аналізувати як екземпляри SolrObject.

**`SolrPingResponse::PARSE_SOLR_DOC`**

Документи слід аналізувати як екземпляри SolrDocument.

## Зміст

-   [SolrPingResponse::construct](solrpingresponse.construct.md) - Конструктор
-   [SolrPingResponse::destruct](solrpingresponse.destruct.md) - Деструктор
-   [SolrPingResponse::getResponse](solrpingresponse.getresponse.md) — Повертає відповідь від сервера
