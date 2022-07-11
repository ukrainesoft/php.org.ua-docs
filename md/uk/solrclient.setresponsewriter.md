- [«SolrClient::rollback](solrclient.rollback.md)
- [SolrClient::setServlet »](solrclient.setservlet.md)

- [PHP Manual](index.md)
- [SolrClient](class.solrclient.md)
- Встановлює письменник відповіді, що використовується для підготовки відповіді
Solr

# SolrClient::setResponseWriter

(PECL solr \>= 0.9.11)

SolrClient::setResponseWriter - Встановлює письменник відповіді,
використовується для підготовки відповіді від Solr

### Опис

public **SolrClient::setResponseWriter**(string `$responseWriter`): void

Встановлює письменник відповіді, що використовується для підготовки відповіді
Solr

### Список параметрів

`responseWriter`
Одне з наступних значень:

- `json`
- `phps`
- `xml`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SolrClient::setResponseWriter()****

` <?php// Це мій власний клас для об'єктівclass SolrClass{   public $_properties = array(); public function __get($property_name) {      if (property_exists($this, $property_name)) {          return $this->$property_name; } else if (isset($_properties[$property_name])) {          return $_properties[$property_name]; }    return null; }}$options = array( 'hostname' => 'localhost',  'port' => 8983, 'path' => '/solr/core1');$client = new SolrClient($op>) setResponseWriter("json");//$response = $client->ping();$query = new SolrQuery();$query->setQuery("*:*");$query->set("objectClassName" , "SolrClass");$query->set("objectPropertiesStorageMode", 1); // 0 для незалежних об'єктів, 1 для суміщенихtry{$response = $client->query($query);$resp = $response->getResponse();print_r($response);print_r($resp); Exception $e) {print_r($e);}?> `
