Перевіряє, чи працює сервер Solr

-   [« SolrClient::optimize](solrclient.optimize.md)
    
-   [SolrClient::query »](solrclient.query.md)
    
-   [PHP Manual](index.md)
    
-   [SolrClient](class.solrclient.md)
    
-   Перевіряє, чи працює сервер Solr
    

# SolrClient::ping

(PECL solr> = 0.9.2)

SolrClient::ping — Перевіряє, чи працює сервер Solr

### Опис

```methodsynopsis
public SolrClient::ping(): SolrPingResponse
```

Перевіряє, чи доступний сервер Solr. Надсилає запит HEAD на сервер Apache Solr.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [SolrPingResponse](class.solrpingresponse.md) у разі успішного виконання або викидає виняток у разі виникнення помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Приклади

**Приклад #1 Приклад використання **SolrClient::ping()****

```php
<?php
$options = array
(
    'hostname' => SOLR_SERVER_HOSTNAME,
    'login'    => SOLR_SERVER_USERNAME,
    'password' => SOLR_SERVER_PASSWORD,
    'port'     => SOLR_SERVER_PORT,
);

$client = new SolrClient($options);

$pingresponse = $client->ping();

?>
```

Результатом виконання цього прикладу буде щось подібне: