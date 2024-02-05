---
navigation:
  - solrupdateresponse.destruct.md: '« SolrUpdateResponse::\_\_destruct'
  - solrpingresponse.construct.md: 'SolrPingResponse::\_\_construct »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrPingResponse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrPingResponse

(PECL solr >= 0.9.2)

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

Рядок необроблених заголовків, надісланих під час запиту

http\_raw\_request

Необроблений запит, надісланий на сервер

http\_raw\_response\_headers

Заголовки відповіді від сервера Solr

http\_raw\_response

Повідомлення у відповідь від сервера

http\_digested\_response

Відповідь у серіалізованому форматі PHP.

## Обумовлені константи

## Константи класу SolrPingResponse

**`SolrPingResponse::PARSE_SOLR_OBJ`**

Документи слід аналізувати як екземпляри SolrObject.

**`SolrPingResponse::PARSE_SOLR_DOC`**

Документи слід аналізувати як екземпляри SolrDocument.

## Зміст

-   [SolrPingResponse::\_\_construct](solrpingresponse.construct.md) \- Конструктор
-   [SolrPingResponse::\_\_destruct](solrpingresponse.destruct.md) \- Деструктор
-   [SolrPingResponse::getResponse](solrpingresponse.getresponse.md)— Повертає відповідь від сервера
