Отримує інформацію про сервер Solr

-   [« SolrClient::setServlet](solrclient.setservlet.md)
    
-   [SolrClient::threads »](solrclient.threads.md)
    
-   [PHP Manual](index.md)
    
-   [SolrClient](class.solrclient.md)
    
-   Отримує інформацію про сервер Solr
    

# SolrClient::system

(PECL solr >= 2.0.0)

SolrClient::system — Отримує інформацію про сервер Solr

### Опис

```methodsynopsis
public SolrClient::system(): void
```

Отримує інформацію про сервер Solr

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [SolrGenericResponse](class.solrgenericresponse.md) у разі успішного виконання.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.