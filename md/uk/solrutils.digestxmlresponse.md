Перетворює XML-рядок відповіді на SolrObject

-   [« SolrUtils](class.solrutils.html)
    
-   [SolrUtils::escapeQueryChars »](solrutils.escapequerychars.html)
    
-   [PHP Manual](index.html)
    
-   [SolrUtils](class.solrutils.html)
    
-   Перетворює XML-рядок відповіді на SolrObject
    

# SolrUtils::digestXmlResponse

(PECL solr> = 0.9.2)

SolrUtils::digestXmlResponse — Перетворює XML-рядок відповіді на SolrObject

### Опис

```methodsynopsis
public static SolrUtils::digestXmlResponse(string $xmlresponse, int $parse_mode = 0): SolrObject
```

Метод перетворює XML-рядок відповіді з сервера Apache Solr SolrObject. У разі помилки викидає виняток SolrException.

### Список параметрів

`xmlresponse`

Рядок відповіді XML від сервера Solr.

`parse_mode`

Використовуйте SolrResponse::PARSESOLROBJ або SolrResponse::PARSESOLRDOC

### Значення, що повертаються

Повертає SolrObject, що представляє відповідь XML.

Якщо для параметра parsemode встановлено значення SolrResponse::PARSESOLROBJ, документи Solr будуть аналізуватись як екземпляри SolrObject.

Якщо встановлено значення SolrResponse::PARSESOLRDOC, вони будуть проаналізовані як екземпляри SolrDocument.