---
navigation:
  - class.solrclient.md: « SolrClient
  - solrclient.adddocuments.md: 'SolrClient::addDocuments »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::addDocument'
---
# SolrClient::addDocument

(PECL solr> = 0.9.2)

SolrClient::addDocument — Додає документ до індексу

### Опис

```methodsynopsis
public SolrClient::addDocument(SolrInputDocument $doc, bool $overwrite = true, int $commitWithin = 0): SolrUpdateResponse
```

Метод додає документ до індексу.

### Список параметрів

`doc`

Примірник SolrInputDocument.

`overwrite`

Чи слід перезаписувати існуючий документ чи ні. Якщо вказано **`false`**, буде дозволено дублікати (кілька документів з однаковим ID).

**Увага**

У PECL Solr < 2.0 $allowDups використовувався замість $overwrite, який виконує самі функції з повністю протилежним прапором bool.

$allowDups = false так само, як і $overwrite = true

`commitWithin`

Кількість мілісекунд для автоматичної фіксації документа. Доступно, починаючи із Solr 1.4. За замовчуванням (0) означає вимкнено.

Якщо значення вказано, залишається контроль над тим, коли робити фіксацію для самого Solr, оптимізуючи кількість коммітів до мінімуму, при цьому дотримуючись вимог до затримки оновлення, і Solr автоматично виконає фіксацію, коли настане найстаріше додавання в буфер.

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.md) або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md)якщо клієнт відмовив або виникла проблема з підключенням.

Викидає [SolrServerException](class.solrserverexception.md)якщо сервер Solr не зміг обробити запит.

### Приклади

**Приклад #1 Приклад використання **SolrClient::addDocument()****

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

$doc = new SolrInputDocument();

$doc->addField('id', 334455);
$doc->addField('cat', 'Software');
$doc->addField('cat', 'Lucene');

$updateResponse = $client->addDocument($doc);

// вам нужно будет зафиксировать изменения, которые будут записаны, если вы не использовали $commitWithin
$client->commit();

print_r($updateResponse->getResponse());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
SolrObject Object
(
    [responseHeader] => SolrObject Object
        (
            [status] => 0
            [QTime] => 1
        )

)
```

**Приклад #2 Приклад використання **SolrClient::addDocument()****

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

$doc = new SolrInputDocument();

$doc->addField('id', 334455);
$doc->addField('cat', 'Software');
$doc->addField('cat', 'Lucene');

// Нет необходимости вызывать commit(), потому что передаётся $commitWithin, поэтому Solr Server будет автоматически фиксировать в течение 10 секунд
$updateResponse = $client->addDocument($doc, false, 10000);

print_r($updateResponse->getResponse());

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
SolrObject Object
(
    [responseHeader] => SolrObject Object
        (
            [status] => 0
            [QTime] => 1
        )

)
```

### Дивіться також

-   [SolrClient::addDocuments()](solrclient.adddocuments.md) - Додає колекцію екземплярів SolrInputDocument до індексу
-   [SolrClient::commit()](solrclient.commit.md) - Завершує всі додавання/видалення, зроблені в індексі
