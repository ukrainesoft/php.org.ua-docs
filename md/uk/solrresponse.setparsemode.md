Встановлює режим аналізу

-   [« SolrResponse::getResponse](solrresponse.getresponse.html)
    
-   [SolrResponse::success »](solrresponse.success.html)
    
-   [PHP Manual](index.html)
    
-   [SolrResponse](class.solrresponse.html)
    
-   Встановлює режим аналізу
    

# SolrResponse::setParseMode

(PECL solr> = 0.9.2)

SolrResponse::setParseMode — Встановлює режим аналізу

### Опис

```methodsynopsis
public SolrResponse::setParseMode(int $parser_mode = 0): bool
```

Встановлює режим аналізу.

### Список параметрів

`parser_mode`

SolrResponse::PARSESOLRDOC аналізує документи в екземплярах SolrDocument. SolrResponse::PARSESOLROBJ розбирає документ на SolrObjects.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.