Екранує рядок запиту Lucene

-   [« SolrUtils::digestXmlResponse](solrutils.digestxmlresponse.html)
    
-   [SolrUtils::getSolrVersion »](solrutils.getsolrversion.html)
    
-   [PHP Manual](index.html)
    
-   [SolrUtils](class.solrutils.html)
    
-   Екранує рядок запиту Lucene
    

# SolrUtils::escapeQueryChars

(PECL solr> = 0.9.2)

SolrUtils::escapeQueryChars — Екранує рядок запиту Lucene

### Опис

```methodsynopsis
public static SolrUtils::escapeQueryChars(string $str): string|false
```

Lucene підтримує екранування спеціальних символів, які є частиною запиту синтаксису.

Поточний список спеціальних символів:

\- && || ! ( ) { } ^ " ~

Ці символи є частиною синтаксису запиту та мають бути екрановані

### Список параметрів

`str`

Рядок запиту, який потрібно екранувати.

### Значення, що повертаються

Повертає екранований рядок або **`false`** у разі виникнення помилки.