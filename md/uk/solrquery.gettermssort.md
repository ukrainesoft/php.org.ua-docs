Повертає ціле число, що вказує, як сортуються вирази

-   [« SolrQuery::getTermsReturnRaw](solrquery.gettermsreturnraw.html)
    
-   [SolrQuery::getTermsUpperBound »](solrquery.gettermsupperbound.html)
    
-   [PHP Manual](index.html)
    
-   [SolrQuery](class.solrquery.html)
    
-   Повертає ціле число, що вказує, як сортуються вирази
    

# SolrQuery::getTermsSort

(PECL solr> = 0.9.2)

SolrQuery::getTermsSort — Повертає ціле число, що вказує, як сортуються вирази

### Опис

```methodsynopsis
public SolrQuery::getTermsSort(): int
```

SolrQuery::TERMSSORTINDEX вказує, що вирази повертаються у порядку індексу. SolrQuery::TERMSSORTCOUNT має на увазі, що вирази сортуються за частотою виразу (спочатку найвищу кількість)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає ціле число та **`null`**, якщо значення не встановлено.