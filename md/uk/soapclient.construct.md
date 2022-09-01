---
navigation:
  - soapclient.call.md: '« SoapClient::call'
  - soapclient.dorequest.md: 'SoapClient::doRequest »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::construct'
---
# SoapClient::construct

(PHP 5, PHP 7, PHP 8)

SoapClient::construct - Конструктор класу SoapClient

### Опис

public **SoapClient::construct**(?string `$wsdl`, array `$options`

Створює об'єкт [SoapClient](class.soapclient.md) для підключення до служби SOAP.

### Список параметрів

`wsdl`

URI WSDL-файлу, який описує сервіс, який використовується для автоматичного налаштування клієнта. Якщо він не вказаний, клієнт працюватиме в режимі без WSDL. mode.

> **Зауваження**
> 
> За промовчанням файл WSDL кешуватиметься для підвищення продуктивності. Щоб вимкнути або налаштувати кешування, дивіться розділ [Опції налаштування SOAP](soap.configuration.html#soap.configuration.list) і [параметр`cache_wsdl`](soapclient.construct.html#soapclient.construct.options.cache-wsdl)

`options`

Асоціативний масив, що визначає додаткові параметри клієнта SOAP. Якщо вказано параметр `wsdl`, це необов'язково, в іншому випадку, принаймні параметри `location` і `url` мають бути вказані.

`location` string

URL-адреса сервера SOAP для надсилання запиту.

Обов'язковий, якщо параметр `wsdl` не вказано. Якщо надано і параметр `wsdl` і `location`, параметр `location` буде пріоритетнішим за розташування, вказаного у WSDL-файлі.

`uri` string

Цільовий простір імен SOAP.

Обов'язковий, якщо параметр `wsdl` не вказано; інакше ігнорується.

`style` int

Визначає стиль зв'язування, який використовуватиме клієнт, використовуючи константи **`SOAP_RPC`** і **`SOAP_DOCUMENT`**. Константа **`SOAP_RPC`** вказує на прив'язку у стилі RPC, де тіло запиту SOAP містить стандартне кодування виклику функції. Константа **`SOAP_DOCUMENT`** вказує на прив'язку в стилі документа, де тіло запиту SOAP містить документ XML з певною службою значенням.

Якщо вказано параметр `wsdl`, цей параметр ігнорується, а стиль зчитується з WSDL-файлу.

Якщо ні цей параметр, ні параметр `wsdl` не вказано, використовується стиль RPC.

`use` int

Визначає стиль кодування, який використовуватиметься клієнтом, використовуючи константи **`SOAP_ENCODED`** або **`SOAP_LITERAL`**. Константа **`SOAP_ENCODED`** вказує на кодування з використанням типів, визначених у специфікації SOAP. Константа **`SOAP_LITERAL`** вказує на кодування з використанням схеми певною службою.

Якщо вказано параметр `wsdl`, цей параметр ігнорується, а кодування прочитується з файлу WSDL.

Якщо ні цей параметр, ні параметр `wsdl` не вказано, використовується стиль "encoded".

`soap_version` int

Визначає версію протоколу SOAP: Константа **`SOAP_1_1`** для SOAP 1.1, або **`SOAP_1_2`** для SOAP 1.2.

Якщо опущено, використовується SOAP 1.1.

`authentication` int

Вказує метод аутентифікації під час використання HTTP-аутентифікації у запитах. Значення може бути або **`SOAP_AUTHENTICATION_BASIC`**, або **`SOAP_AUTHENTICATION_DIGEST`**

Якщо параметр не вказано, але вказано параметр `login`використовується Basic Authentication.

`login` string

Ім'я користувача для використання під час аутентифікації HTTP Basic або Digest.

`password` string

Пароль для використання під час аутентифікації HTTP Basic або Digest.

Не слід плутати з параметром `passphrase`, який використовується для автентифікації сертифіката клієнта HTTPS.

`local_cert` string

Шлях до сертифіката клієнта для використання з автентифікацією HTTPS. Повинен бути файл у кодуванні PEM, що містить сертифікат та закритий ключ.

Файл також може включати ланцюжок емітентів, який повинен йти після сертифікату клієнта.

Також може бути задано за допомогою параметра [`stream_context`](soapclient.construct.html#soapclient.construct.options.stream-context), який також підтримує вказівку окремого файлу закритого ключа.

`passphrase` string

Ключова фраза для сертифіката клієнта, вказаного у параметрі `local_cert`

Не слід плутати з параметром `password`який використовується для аутентифікації Basic або Digest.

Можна також встановити за допомогою параметра [`stream_context`](soapclient.construct.html#soapclient.construct.options.stream-context)

`proxy_host` string

Ім'я хоста для використання як проксі-сервер для HTTP-запитів.

Також має бути зазначений параметр `proxy_port`

`proxy_port` int

TCP-порт для використання при підключенні до проксі-сервера, вказаному у параметрі `proxy_host`

`proxy_login` string

Необов'язкове ім'я користувача для аутентифікації на проксі-сервері, вказаному у параметрі `proxy_host`за допомогою HTTP Basic Authentication.

`proxy_password` string

Необов'язковий пароль для аутентифікації на проксі-сервері, вказаному у параметрі `proxy_host`за допомогою HTTP Basic Authentication.

`compression` int

Включає стиснення HTTP SOAP запитів та відповідей.

Значення має бути побітовим АБО з трьох частин: необов'язкова \*\*`SOAP_COMPRESSION_ACCEPT`\*\*для надсилання заголовка "Accept-Encoding"; або константа **`SOAP_COMPRESSION_GZIP`** або **`SOAP_COMPRESSION_DEFLATE`** для вказівки використовуваного алгоритму стискування; число від 1 до 9, щоб вказати рівень стиснення, який використовуватиметься у запиті. Наприклад, щоб увімкнути двосторонній стиск gzip з максимальним рівнем стиснення, використовуйте `SOAP_COMPRESSION_ACCEPT | SOAP_COMPRESSION_GZIP | 9`

`encoding` string

Визначає внутрішнє кодування символів. Запити завжди надсилаються в UTF-8 і перетворюються на це кодування і назад.

`trace` bool

Захоплює інформацію про запит та відповідь, яка потім може бути доступна за допомогою методів: **SoapClient::getLastRequest()** **SoapClient::getLastRequestHeaders()** **SoapClient::getLastResponse()**, або **SoapClient::getLastResponseHeaders()**

Якщо опущено, використовується значення за замовчуванням **`false`**

`classmap` array

Використовується для зіставлення типів, визначених у WSDL із класами PHP. Має бути вказаний асоціативний масив (array) з іменами типів з WSDL як ключі та іменами класів PHP як значень. Зверніть увагу, що назва типу елемента не обов'язково збігається з ім'ям елемента (тега).

Надані імена класів завжди повинні бути повністю визначені за допомогою будь-яких [просторів імен](language.namespaces.md) і ніколи не повинні починатися з ведучого слєша (`\`). Правильна форма може бути вказана за допомогою [::class](language.oop5.basic.html#language.oop5.basic.class.class)

Зверніть увагу, що при створенні класу конструктор не викликатиметься, але магічні методи [set()](language.oop5.overloading.html#object.set) і [get()](language.oop5.overloading.html#object.get) будуть викликатися окремих властивостей.

`typemap` array

Використовується для визначення зіставлень типів за допомогою визначених користувачем callback-функцій. Кожне зіставлення типів повинно бути масивом з ключами. `type_name` (Рядок (string), що визначає тип елемента XML); `type_ns` (рядок (string), що містить простір імен URI); `from_xml` [callable](language.types.callable.md), що приймає один рядковий параметр і повертає об'єкт) і `to_xml` [callable](language.types.callable.md), що приймає один об'єктний параметр і повертає рядок).

`exceptions` bool

Визначає, чи помилки викидатимуть виняток типу [SoapFault](class.soapfault.md)

За замовчуванням значення **`true`**

`connection_timeout` int

Визначає час очікування в секундах для підключення до SOAP. Параметр не визначає час очікування служб із повільними відповідями. Щоб обмежити час очікування завершення дзвінків, можна налаштувати конфігурацію. [defaultsockettimeout](filesystem.configuration.html#ini.default-socket-timeout)

`cache_wsdl` int

Якщо вказано параметр `wsdl`, а також параметр [soap.wsdlcacheenabled](soap.configuration.html#ini.soap.wsdl-cache-enabled) Увімкнено, цей параметр визначає тип кешування. Одне із значень: **`WSDL_CACHE_NONE`** **`WSDL_CACHE_DISK`** **`WSDL_CACHE_MEMORY`** або **`WSDL_CACHE_BOTH`**

Доступні два типи кешу: кешування у пам'яті, яке кешує WSDL у пам'яті поточного процесу та дискове кешування, яке кешує WSDL у файлі на диску, що поділяється між усіма процесами. Каталог, який використовуватиметься для дискового кешу, визначається параметром [soap.wsdlcachedir](soap.configuration.html#ini.soap.wsdl-cache-dir). Обидва кеші використовують однаковий час життя, що визначається параметром [soap.wsdlcachettl](soap.configuration.html#ini.soap.wsdl-cache-ttl). У кеша в пам'яті також є максимальна кількість записів, що визначається параметром [soap.wsdlcachelimit](soap.configuration.html#ini.soap.wsdl-cache-limit)

Якщо не вказано, використовуватиметься параметр конфігурації [soap.wsdlcache](soap.configuration.html#ini.soap.wsdl-cache)

`user_agent` string

Значення для використання в заголовку HTTP `User-Agent` під час виконання запитів.

Можна також встановити за допомогою параметра [`stream_context`](soapclient.construct.html#soapclient.construct.options.stream-context)

Якщо не вказано, User-Agent буде `"PHP-SOAP/"` за яким слідує значення **`PHP_VERSION`**

`stream_context` resource

Контекст [stream context](context.md), створений за допомогою функції [streamcontextcreate()](function.stream-context-create.md), яка дає змогу встановити додаткові параметри.

Контекст може містити [параметри контексту сокету](context.socket.md) [параметри контексту SSL](context.ssl.md), а також вибрані [опции контекста HTTP](context.http.md) `content_type` `header` `max_redirects` `protocol_version`, і `user_agent`

Зверніть увагу, що наступні заголовки HTTP генеруються автоматично або на основі інших параметрів і будуть ігноруватися, якщо вказані в параметрі контексту `'header'` `host` `connection` `user-agent` `content-length` `content-type` `cookie` `authorization` і `proxy-authorization`

`features` int

Бітова маска для включення однієї або кількох таких функцій:

**`SOAP_SINGLE_ELEMENT_ARRAYS`**

При декодуванні відповіді масив за замовчуванням визначається, чи з'являється ім'я елемента один чи кілька разів у певному батьківському елементі. Для елементів, які з'являються лише один раз, властивість об'єкта дозволяє отримати прямий доступ до вмісту; для елементів, які з'являються більше одного разу, властивість містить масив із вмістом кожного відповідного елемента.

Якщо увімкнено функцію **`SOAP_SINGLE_ELEMENT_ARRAYS`**, елементи, які з'являються лише один раз, поміщаються в одноелементний масив, щоб доступ був послідовним для всіх елементів. Це буде працювати тільки при використанні WSDL, що містить схему відповіді. Для демонстрації дивіться розділ із прикладами.

**`SOAP_USE_XSI_ARRAY_TYPE`**

Якщо [параметру`use`](soapclient.construct.html#soapclient.construct.options.use) або властивості WSDL передано значення `encoded`, масиви примусово використовують тип `SOAP-ENC:Array`, а чи не специфічний для схеми.

**`SOAP_WAIT_ONE_WAY_CALLS`**

Очікування відповіді, навіть якщо WSDL вказує на односторонній запит.

`keep_alive` bool

Логічне значення, що визначає, чи слід надсилати заголовок `Connection: Keep-Alive` або `Connection: close`

За замовчуванням **`true`**

`ssl_method` string

Визначає версію протоколу SSL або TLS для використання у захищених з'єднаннях HTTP замість узгодження за промовчанням. Вказівка **`SOAP_SSL_METHOD_SSLv2`** або **`SOAP_SSL_METHOD_SSLv3`** змусить використовувати SSL 2 або SSL 3 відповідно. Вказівка ​​константи **`SOAP_SSL_METHOD_SSLv23`** немає сенсу; константа існує лише зворотної сумісності. Починаючи з PHP 7.2, вказівка ​​константи **`SOAP_SSL_METHOD_TLS`** також немає сенсу; у попередніх версіях константа визначала примусове використання TLS 1.0.

Зверніть увагу, що SSL версій 2 і 3 вважаються небезпечними і можуть не підтримуватись встановленою бібліотекою OpenSSL.

Параметр оголошено *Застарілим*починаючи з PHP 8.1.0. Більш гнучкою альтернативою, яка дозволяє вказувати окремі версії TLS, можна використовувати параметр [`stream_context`](soapclient.construct.html#soapclient.construct.options.stream-context) з параметром контексту 'cryptoметод'.

**Приклад #1 Вказівка ​​використання тільки TLS 1.3**

```php
<?php
$context = stream_context_create([
    'ssl' => [
        'crypto_method' => STREAM_CRYPTO_METHOD_TLSv1_3_CLIENT
     ]
];
$client = new SoapClient("some.wsdl", ['context' => $context]);
```

### Помилки

Метод **SoapClient::construct()** виводить помилку рівня **`E_ERROR`**, якщо параметри `location` і `uri` не вказано у режимі не-WSDL.

Викидається виняток [SoapFault](class.soapfault.md), якщо параметр `wsdl` URI не може бути завантажено.

### Приклади

**Приклад #2 Приклад використання **SoapClient::construct()****

```php
<?php

$client = new SoapClient("some.wsdl");

$client = new SoapClient("some.wsdl", array('soap_version'   => SOAP_1_2));

$client = new SoapClient("some.wsdl", array('login'          => "some_name",
                                            'password'       => "some_password"));

$client = new SoapClient("some.wsdl", array('proxy_host'     => "localhost",
                                            'proxy_port'     => 8080));

$client = new SoapClient("some.wsdl", array('proxy_host'     => "localhost",
                                            'proxy_port'     => 8080,
                                            'proxy_login'    => "some_name",
                                            'proxy_password' => "some_password"));

$client = new SoapClient("some.wsdl", array('local_cert'     => "cert_key.pem"));

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/",
                                     'style'    => SOAP_DOCUMENT,
                                     'use'      => SOAP_LITERAL));

$client = new SoapClient("some.wsdl",
  array('compression' => SOAP_COMPRESSION_ACCEPT | SOAP_COMPRESSION_GZIP | 9));

$client = new SoapClient("some.wsdl", array('encoding'=>'ISO-8859-1'));

class MyBook {
    public $title;
    public $author;
}

$client = new SoapClient("books.wsdl", array('classmap' => array('book' => "MyBook")));

$typemap = array(
    array("type_ns"  => "http://schemas.example.com",
         "type_name" => "book",
         "from_xml"  => "unserialize_book",
         "to_xml"    => "serialize_book")
);
$client = new SoapClient("books.wsdl", array('typemap' => $typemap));

?>
```

**Приклад #3 Приклад використання **`SOAP_SINGLE_ELEMENT_ARRAYS`****

```php
/* Предполагая, что ответ, подобный этому, и соответствующий WSDL:
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns="urn:example">
    <SOAP-ENV:Body>
        <response>
            <collection>
                <item>Single</item>
            </collection>
            <collection>
                <item>First</item>
                <item>Second</item>
            </collection>
        </response>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
*/

echo "По умолчанию:\n";

$client = new TestSoapClient(__DIR__ . '/temp.wsdl');
$response = $client->exampleRequest();
var_dump( $response->collection[0]->item );
var_dump( $response->collection[1]->item );

echo "\nС помощью SOAP_SINGLE_ELEMENT_ARRAYS:\n";

$client = new TestSoapClient(__DIR__ . '/temp.wsdl', ['features' => SOAP_SINGLE_ELEMENT_ARRAYS]);
$response = $client->exampleRequest();
var_dump( $response->collection[0]->item );
var_dump( $response->collection[1]->item );
```

Результат виконання цього прикладу:

```
По умолчанию:
string(6) "Single"
array(2) {
  [0] =>
  string(5) "First"
  [1] =>
  string(6) "Second"
}

С помощью SOAP_SINGLE_ELEMENT_ARRAYS:
array(1) {
  [0] =>
  string(6) "Single"
}
array(2) {
  [0] =>
  string(5) "First"
  [1] =>
  string(6) "Second"
}
```
