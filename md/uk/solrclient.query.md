- [«SolrClient::ping](solrclient.ping.md)
- [SolrClient::request »](solrclient.request.md)

- [PHP Manual](index.md)
- [SolrClient](class.solrclient.md)
- Надсилає запит на сервер

# SolrClient::query

(PECL solr \> = 0.9.2)

SolrClient::query — Надсилає запит на сервер

### Опис

public **SolrClient::query**([SolrParams](class.solrparams.md)
`$query`): [SolrQueryResponse](class.solrqueryresponse.md)

Надсилає запит на сервер.

### Список параметрів

`query`
Об'єкт [SolrParams](class.solrparams.md). Для складних запитів
рекомендується використовувати [SolrQuery](class.solrquery.md).

### Значення, що повертаються

Повертає об'єкт [SolrQueryResponse](class.solrqueryresponse.md) у
у разі успішного виконання або викидає виняток у разі
виникнення помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md), якщо
клієнт відмовив чи виникла проблема із підключенням.

Викидає [SolrServerException](class.solrserverexception.md), якщо
сервер Solr не зміг обробити запит.

### Приклади

**Приклад #1 Приклад використання **SolrClient::query()****

`<?php$options = array(   'hostname' => 'localhost',   'login'    => 'username',    'password' =>                 new SolrClient($options);$query = new SolrQuery();$query->setQuery('lucene');$query->setStart(0);$query->setRows(50);$query->addField( 'cat')->addField('features')->addField('id')->addField('timestamp');$query_response = $client->query($query);$response = $query_response->getResponse ();print_r($response);?> `

Результатом виконання цього прикладу буде щось подібне:

SolrObject Object
(
[responseHeader] => SolrObject Object
(
[status] => 0
[QTime] => 3
[params] => SolrObject Object
(
[fl] => cat,features,id,timestamp
[indent] => on
[start] => 0
[q] => lucene
[wt] => xml
[version] => 2.2
[rows] => 50
)

)

[response] => SolrObject Object
(
[numFound] => 1
[start] => 0
[docs] => Array
(
[0] => SolrObject Object
(
[id] => SOLR1000
[cat] => Array
(
[0] => software
[1] => search
)

[features] => Array
(
[0] => Advanced Full-Text Search Capabilities using Lucene
[1] => Optimized for High Volume Web Traffic
[2] => Standards Based Open Interfaces - XML and HTTP
[3] => Comprehensive HTML Administration Interfaces
[4] => Scalability - Efficient Replication to other Solr Search Servers
[5] => Flexible and Adaptable with XML configuration and Schema
[6] => Good unicode support: héllo (hello with an accent over the e)
)

)

)

)

)
