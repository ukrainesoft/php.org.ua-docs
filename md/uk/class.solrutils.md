Клас SolrUtils

-   [« Примеры](solr.examples.html)
    
-   [SolrUtils::digestXmlResponse »](solrutils.digestxmlresponse.html)
    
-   [PHP Manual](index.html)
    
-   [Solr](book.solr.html)
    
-   Клас SolrUtils
    

# Клас SolrUtils

(PECL solr> = 0.9.2)

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

-   [SolrUtils::digestXmlResponse](solrutils.digestxmlresponse.html) — Перетворює XML-рядок відповіді на SolrObject
-   [SolrUtils::escapeQueryChars](solrutils.escapequerychars.html) — Екранує рядок запиту Lucene
-   [SolrUtils::getSolrVersion](solrutils.getsolrversion.html) — Повертає поточну версію модуля Solr
-   [SolrUtils::queryPhrase](solrutils.queryphrase.html) — Підготовка фрази з неекранованого рядка запиту Lucene