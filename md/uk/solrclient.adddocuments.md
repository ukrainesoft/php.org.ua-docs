- [« SolrClient::addDocument](solrclient.adddocument.md)
- [SolrClient::commit »](solrclient.commit.md)

- [PHP Manual](index.md)
- [SolrClient](class.solrclient.md)
- Додає колекцію екземплярів SolrInputDocument до індексу

# SolrClient::addDocuments

(PECL solr \> = 0.9.2)

SolrClient::addDocuments — Додає колекцію екземплярів
SolrInputDocument в індекс

### Опис

public **SolrClient::addDocuments**(array `$docs`, bool `$overwrite` =
**`true`**, int `$commitWithin` = 0): void

Додає колекцію документів до індексу.

### Список параметрів

`docs`
Масив, що містить колекцію екземплярів SolrInputDocument. Цей масив
має бути реальною змінною.

`overwrite`
Чи варто перезаписувати існуючі документи чи ні. Якщо вказано
значення **`false`**, будуть дозволені дублікати (кілька документів з
однаковим ID).

**Увага**
У PECL Solr \< 2.0 $allowDups використовувався замість $overwrite, який
виконує самі функції з повністю протилежним прапором bool.

$allowDups = false так само, як і $overwrite = true

`commitWithin`
Кількість мілісекунд для автоматичної фіксації документа. Доступно,
починаючи із Solr 1.4. За промовчанням (0) означає вимкнено.

Якщо значення вказано, залишається контроль над тим, коли робити фіксацію
для самого Solr, оптимізуючи кількість коммітів до мінімуму, причому
дотримуючись вимог до затримки оновлення, і Solr автоматично виконає
фіксацію, коли настане найстаріше додавання до буфера.

### Значення, що повертаються

Повертає об'єкт [SolrUpdateResponse](class.solrupdateresponse.md)
або викидає виняток у разі помилки.

### Помилки

Викидає [SolrClientException](class.solrclientexception.md), якщо
клієнт відмовив чи виникла проблема із підключенням.

Викидає [SolrServerException](class.solrserverexception.md), якщо
сервер Solr не зміг обробити запит.

### Приклади

**Приклад #1 Приклад використання **SolrClient::addDocuments()****

` <?php$options = array(    'hostname' => SOLR_SERVER_HOSTNAME,    'login'    => SOLR_SERVER_USERNAME,    'password' => SOLR_SERVER_PASSWORD,    'port'     => SOLR_SERVER_PORT,);$client = new SolrClient($options);$ doc = new SolrInputDocument();$doc->addField('id', 334455);$doc->addField('cat', 'Software');$doc->addField('cat', 'Lucene'); $doc2==clone $doc;$doc2->deleteField('id');$doc2->addField('id', 334456);$docs = array($doc, $doc2);$updateResponse = $client-> addDocuments($docs);// ніякі зміни не будуть записані на диск, якщо не буде переданий $commitWithin або не буде викликаний SolrClient::commitprint_r($upda>)

Результатом виконання цього прикладу буде щось подібне:

SolrObject Object
(
[responseHeader] => SolrObject Object
(
[status] => 0
[QTime] => 2
)

)

### Дивіться також

- [SolrClient::addDocument()](solrclient.adddocument.md) - Додає
документ в індекс
- [SolrClient::commit()](solrclient.commit.md) - Завершує все
додавання/видалення, зроблені в індексі
