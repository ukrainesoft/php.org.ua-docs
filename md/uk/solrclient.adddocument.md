- [«SolrClient](class.solrclient.md)
- [SolrClient::addDocuments »](solrclient.adddocuments.md)

- [PHP Manual](index.md)
- [SolrClient](class.solrclient.md)
- Додає документ до індексу

# SolrClient::addDocument

(PECL solr \> = 0.9.2)

SolrClient::addDocument — Додає документ до індексу

### Опис

public
**SolrClient::addDocument**([SolrInputDocument](class.solrinputdocument.md)
`$doc`, bool `$overwrite` = **`true`**, int `$commitWithin` = 0):
[SolrUpdateResponse](class.solrupdateresponse.md)

Метод додає документ до індексу.

### Список параметрів

`doc`
Примірник SolrInputDocument.

`overwrite`
Чи слід перезаписувати існуючий документ чи ні. Якщо вказано
**`false`**, будуть дозволені дублікати (кілька документів з
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

**Приклад #1 Приклад використання **SolrClient::addDocument()****

` <?php$options = array(    'hostname' => SOLR_SERVER_HOSTNAME,    'login'    => SOLR_SERVER_USERNAME,    'password' => SOLR_SERVER_PASSWORD,    'port'     => SOLR_SERVER_PORT,);$client = new SolrClient($options);$ doc = new SolrInputDocument();$doc->addField('id', 334455);$doc->addField('cat', 'Software');$doc->addField('cat', 'Lucene'); $updateResponse==$client->addDocument($doc);// вам потрібно зафіксувати зміни, будуть записані, якщо ви не використовували $commitWithin$client-s> ?> `

Результатом виконання цього прикладу буде щось подібне:


SolrObject Object
(
[responseHeader] => SolrObject Object
(
[status] => 0
[QTime] => 1
)

)

**Приклад #2 Приклад використання **SolrClient::addDocument()** #2**

` <?php$options = array(    'hostname' => SOLR_SERVER_HOSTNAME,    'login'    => SOLR_SERVER_USERNAME,    'password' => SOLR_SERVER_PASSWORD,    'port'     => SOLR_SERVER_PORT,);$client = new SolrClient($options);$ doc = new SolrInputDocument();$doc->addField('id', 334455);$doc->addField('cat', 'Software');$doc->addField('cat', 'Lucene'); // Нет необхідності викликати commit(), потому передається $commitWithin, тому Solr Server буде автоматично фіксувати в протягом 10 секунд$updateResponse <$>| ));?> `

Результатом виконання цього прикладу буде щось подібне:


SolrObject Object
(
[responseHeader] => SolrObject Object
(
[status] => 0
[QTime] => 1
)

)

### Дивіться також

- [SolrClient::addDocuments()](solrclient.adddocuments.md) -
Додає колекцію екземплярів SolrInputDocument до індексу
- [SolrClient::commit()](solrclient.commit.md) - Завершує все
додавання/видалення, зроблені в індексі
