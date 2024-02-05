---
navigation:
  - solr.examples.md: « Приклади
  - solrutils.digestxmlresponse.md: 'SolrUtils::digestXmlResponse »'
  - index.md: PHP Manual
  - book.solr.md: Solr
title: Клас SolrUtils
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SolrUtils

(PECL solr >= 0.9.2)

## Вступ

Містить службові методи для отримання поточної версії модуля та підготовки фраз запиту.

Також містить метод для екранування рядків запиту та аналізу відповідей XML.

## Огляд класів

```classsynopsis



    
     
      abstract
      class SolrUtils
     
     {


    /* Методы */
    
   public static digestXmlResponse(string $xmlresponse, int $parse_mode = 0): SolrObject
public static escapeQueryChars(string $str): string|false
public static getSolrVersion(): string
public static queryPhrase(string $str): string

   }
```

## Зміст

-   [SolrUtils::digestXmlResponse](solrutils.digestxmlresponse.md)— Перетворює XML-рядок відповіді на об'єкт SolrObject
-   [SolrUtils::escapeQueryChars](solrutils.escapequerychars.md)— Екранує рядок запиту Lucene
-   [SolrUtils::getSolrVersion](solrutils.getsolrversion.md)— Повертає поточну версію модуля Solr
-   [SolrUtils::queryPhrase](solrutils.queryphrase.md)— Підготовка фрази з неекранованого рядка запиту Lucene
