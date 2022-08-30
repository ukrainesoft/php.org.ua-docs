Повертає внутрішню інформацію про те, де було викинуто виняток

-   [« SolrClientException](class.solrclientexception.md)
    
-   [SolrServerException »](class.solrserverexception.md)
    
-   [PHP Manual](index.md)
    
-   [SolrClientException](class.solrclientexception.md)
    
-   Повертає внутрішню інформацію про те, де було викинуто виняток
    

# SolrClientException::getInternalInfo

(PECL solr> = 0.9.2)

SolrClientException::getInternalInfo — Повертає внутрішню інформацію про те, де було викинуто виняток

### Опис

```methodsynopsis
public SolrClientException::getInternalInfo(): array
```

Повертає внутрішню інформацію про те, де було викинуто виняток.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить внутрішню інформацію про те, де була викликана помилка. Використовується лише для налагодження розробниками модулів.