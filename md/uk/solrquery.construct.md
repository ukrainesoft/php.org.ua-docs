Конструктор

-   [« SolrQuery::collapse](solrquery.collapse.html)
    
-   [SolrQuery::destruct »](solrquery.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Конструктор
    

# SolrQuery::construct

(PECL solr> = 0.9.2)

SolrQuery::construct — Конструктор

### Опис

public **SolrQuery::construct**(string `$q`

Конструктор.

### Список параметрів

`q`

Додатковий пошуковий запит

### Значення, що повертаються

Нічого

### Помилки

Викидає [SolrIllegalArgumentException](class.solrillegalargumentexception.html) у разі передачі неприпустимого параметра.

### список змін

| Версия | Описание |
| --- | --- |
| PECL solr 2.0.0 | Якщо `q` був неприпустимим, викидається виняток [SolrIllegalArgumentException](class.solrillegalargumentexception.html). Раніше видавалась помилка. |