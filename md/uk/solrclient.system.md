Отримує інформацію про сервер Solr

-   [« SolrClient::setServlet](solrclient.setservlet.html)
    
-   [SolrClient::threads »](solrclient.threads.html)
    
-   [PHP Manual](index.html)
    
-   [SolrClient](class.solrclient.html)
    
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

Повертає об'єкт [SolrGenericResponse](class.solrgenericresponse.html) у разі успішного виконання.

### Помилки

Викидає [SolrClientException](class.solrclientexception.html)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.html)якщо сервер Solr не зміг обробити запит.