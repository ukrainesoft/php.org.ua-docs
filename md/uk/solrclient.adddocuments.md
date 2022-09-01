---
navigation:
  - solrclient.adddocument.md: '« SolrClient::addDocument'
  - solrclient.commit.md: 'SolrClient::commit »'
  - index.md: PHP Manual
  - class.solrclient.md: SolrClient
title: 'SolrClient::addDocuments'
---
# SolrClient::addDocuments

(PECL solr> = 0.9.2)

SolrClient::addDocuments — Додає колекцію екземплярів SolrInputDocument до індексу

### Опис

```methodsynopsis
public SolrClient::addDocuments(array $docs, bool $overwrite = true, int $commitWithin = 0): void
```

Додає колекцію документів до індексу.

### Список параметрів

`docs`

Масив, що містить колекцію екземплярів SolrInputDocument. Цей масив має бути реальною змінною.

`overwrite`

Чи варто перезаписувати існуючі документи чи ні. Якщо вказано значення **`false`**, буде дозволено дублікати (кілька документів з однаковим ID).

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

**Приклад #1 Приклад використання **SolrClient::addDocuments()****

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

$doc2 = clone $doc;

$doc2->deleteField('id');
$doc2->addField('id', 334456);

$docs = array($doc, $doc2);

$updateResponse = $client->addDocuments($docs);

// никакие изменения не будут записаны на диск, если не будет передан $commitWithin или не будет вызван SolrClient::commit

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
            [QTime] => 2
        )

)
```

### Дивіться також

-   [SolrClient::addDocument()](solrclient.adddocument.md) - Додає документ до індексу
-   [SolrClient::commit()](solrclient.commit.md) - Завершує всі додавання/видалення, зроблені в індексі
