---
navigation:
  - soapclient.call.md: '« SoapClient::\_\_call'
  - soapclient.dorequest.md: 'SoapClient::\_\_doRequest »'
  - index.md: PHP Manual
  - class.soapclient.md: SoapClient
title: 'SoapClient::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SoapClient::\_\_construct

(PHP 5, PHP 7, PHP 8)

SoapClient::\_\_construct - Конструктор класу SoapClient

### Опис

public **SoapClient::\_\_construct**(?string`$wsdl`, array`$options` \[\]) .

Створює об'єкт [SoapClient](class.soapclient.md)для подключения к службе SOAP.

### Список параметрів

`wsdl`

URI WSDL-файлу, який описує сервіс, який використовується для автоматичного налаштування клієнта. Якщо він не вказаний, клієнт працюватиме в режимі без WSDL. mode.

> **Зауваження** :
> 
> За промовчанням файл WSDL кешуватиметься для підвищення продуктивності. Щоб вимкнути або налаштувати кешування, див. розділ Опції налаштування SOAP та [параметр`cache_wsdl`](soapclient.construct.md#soapclient.construct.options.cache-wsdl)

`options`

Асоціативний масив, що визначає додаткові параметри клієнта SOAP. Якщо вказано параметр `wsdl`, це необов'язково, в іншому випадку, принаймні параметри `location`и`url` мають бути вказані.

`location`string

URL-адреса сервера SOAP для надсилання запиту.

Обязателен, если параметр`wsdl` не вказано. Якщо надано і параметр `wsdl`и`location`, параметр`location` буде пріоритетнішим за розташування, зазначене у WSDL-файлі.

`uri`string

Цільовий простір імен SOAP.

Обязателен, если параметр`wsdl` не вказано; інакше ігнорується.

`style`int

Визначає стиль зв'язування, який використовуватиме клієнт, використовуючи константи **`SOAP_RPC`** і **`SOAP_DOCUMENT`**Константа**`SOAP_RPC`** вказує на прив'язку у стилі RPC, де тіло запиту SOAP містить стандартне кодування виклику функції. Константа **`SOAP_DOCUMENT`** вказує на прив'язку в стилі документа, де тіло запиту SOAP містить документ XML з певною службою значенням.

Если указан параметр`wsdl`, цей параметр ігнорується, а стиль зчитується з WSDL-файлу.

Якщо ні цей параметр, ні параметр `wsdl` не вказано, використовується стиль RPC.

`use`int

Визначає стиль кодування, який використовуватиметься клієнтом, використовуючи константи **`SOAP_ENCODED`** або **`SOAP_LITERAL`**Константа**`SOAP_ENCODED`** вказує на кодування з використанням типів, визначених у специфікації SOAP. Константа **`SOAP_LITERAL`** вказує на кодування з використанням схеми певною службою.

Если указан параметр`wsdl`, цей параметр ігнорується, а кодування зчитується з файлу WSDL.

Якщо ні цей параметр, ні параметр `wsdl` не вказано, використовується стиль "encoded".

`soap_version`int

Визначає версію протоколу SOAP: Константа \*\*`SOAP_1_1`**для SOAP 1.1, или**`SOAP_1_2`\*\*для SOAP 1.2.

Якщо опущено, використовується SOAP 1.1.

`authentication`int

Вказує метод аутентифікації під час використання HTTP-аутентифікації у запитах. Значення може бути або **`SOAP_AUTHENTICATION_BASIC`**, либо\*\*`SOAP_AUTHENTICATION_DIGEST`\*\*

Якщо параметр не вказано, але вказано параметр `login`використовується Basic Authentication.

`login`string

Ім'я користувача для використання під час аутентифікації HTTP Basic або Digest.

`password`string

Пароль для використання під час аутентифікації HTTP Basic або Digest.

Не слід плутати з параметром `passphrase`, який використовується для автентифікації сертифіката клієнта HTTPS.

`local_cert`string

Шлях до сертифіката клієнта для використання з автентифікацією HTTPS. Має бути файл у кодуванні PEM, що містить сертифікат і закритий ключ.

Файл також може включати ланцюжок емітентів, який повинен йти після сертифіката клієнта.

Також може бути задано за допомогою параметра [`stream_context`](soapclient.construct.md#soapclient.construct.options.stream-context), який також підтримує вказівку окремого файлу закритого ключа.

`passphrase`string

Ключевая фраза для клиентского сертификата, указанного в параметре`local_cert`

Не слід плутати з параметром `password`який використовується для аутентифікації Basic або Digest.

Можно также установить с помощью параметра[`stream_context`](soapclient.construct.md#soapclient.construct.options.stream-context)

`proxy_host`string

Ім'я хоста для використання як проксі-сервер для HTTP-запитів.

Також має бути зазначений параметр `proxy_port`

`proxy_port`int

TCP-порт для использования при подключении к прокси-серверу, указанному в параметре`proxy_host`

`proxy_login`string

Необов'язкове ім'я користувача для аутентифікації на проксі-сервері, вказаному у параметрі `proxy_host`за допомогою HTTP Basic Authentication.

`proxy_password`string

Необов'язковий пароль для аутентифікації на проксі-сервері, вказаному у параметрі `proxy_host`за допомогою HTTP Basic Authentication.

`compression`int

Включає стиснення HTTP SOAP запитів та відповідей.

Значення має бути побітовим АБО з трьох частин: необов'язкова \*\*`SOAP_COMPRESSION_ACCEPT`\*\*для надсилання заголовка "Accept-Encoding"; або константа **`SOAP_COMPRESSION_GZIP`** або **`SOAP_COMPRESSION_DEFLATE`** для вказівки використовуваного алгоритму стискування; число від 1 до 9, щоб вказати рівень стиснення, який використовуватиметься у запиті. Наприклад, щоб увімкнути двосторонній стиск gzip з максимальним рівнем стиснення, використовуйте `SOAP_COMPRESSION_ACCEPT | SOAP_COMPRESSION_GZIP | 9`

`encoding`string

Визначає внутрішнє кодування символів. Запити завжди надсилаються в UTF-8 і перетворюються на це кодування і назад.

`trace`bool

Захоплює інформацію про запит та відповідь, яка потім може бути доступна за допомогою методів: [SoapClient::\_\_getLastRequest()](soapclient.getlastrequest.md) [SoapClient::\_\_getLastRequestHeaders()](soapclient.getlastrequestheaders.md) [SoapClient::\_\_getLastResponse()](soapclient.getlastresponse.md) і [SoapClient::\_\_getLastResponseHeaders()](soapclient.getlastresponseheaders.md)

Если опущено, по умолчанию используется значение\*\*`false`\*\*

`classmap`array

Використовується для зіставлення типів, визначених у WSDL із класами PHP. Має бути вказаний асоціативний масив (array) з іменами типів з WSDL як ключі та іменами класів PHP як значень. Зверніть увагу, що назва типу елемента не обов'язково збігається з ім'ям елемента (тега).

Надані імена класів завжди повинні бути повністю визначені за допомогою будь-яких [просторів імен](language.namespaces.md) і ніколи не повинні починатися з ведучого слєша (`\`). Правильна форма може бути вказана за допомогою [::class](language.oop5.basic.md#language.oop5.basic.class.class)

Зверніть увагу, що при створенні класу конструктор не викликатиметься, але магічні методи [\_\_set()](language.oop5.overloading.md#object.set) і [\_\_get()](language.oop5.overloading.md#object.get) будуть викликатися окремих властивостей.

`typemap`array

Використовується для визначення зіставлень типів за допомогою визначених користувачем callback-функцій. Кожне зіставлення типів повинно бути масивом з ключами. `type_name` (Рядок (string), що визначає тип елемента XML); `type_ns` (рядок (string), що містить простір імен URI); `from_xml` [callable](language.types.callable.md), що приймає один рядковий параметр і повертає об'єкт) і `to_xml` [callable](language.types.callable.md), що приймає один об'єктний параметр і повертає рядок).

`exceptions`bool

Визначає, чи помилки викидатимуть виняток типу [SoapFault](class.soapfault.md)

По умолчанию значение\*\*`true`\*\*

`connection_timeout`int

Визначає час очікування в секундах для підключення до SOAP. Параметр не визначає час очікування служб із повільними відповідями. Щоб обмежити час очікування завершення дзвінків, можна налаштувати конфігурацію. [default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout)

`cache_wsdl`int

Если указан параметр`wsdl`, а также параметр[soap.wsdl\_cache\_enabled](soap.configuration.md#ini.soap.wsdl-cache-enabled) Увімкнено, цей параметр визначає тип кешування. Одне із значень: **`WSDL_CACHE_NONE`** **`WSDL_CACHE_DISK`** **`WSDL_CACHE_MEMORY`** або **`WSDL_CACHE_BOTH`**

Доступні два типи кешу: кешування у пам'яті, яке кешує WSDL у пам'яті поточного процесу та дискове кешування, яке кешує WSDL у файлі на диску, що поділяється між усіма процесами. Каталог, який використовуватиметься для дискового кешу, визначається параметром [soap.wsdl\_cache\_dir](soap.configuration.md#ini.soap.wsdl-cache-dir)Оба кеша используют одинаковое время жизни, определяемое параметром[soap.wsdl\_cache\_ttl](soap.configuration.md#ini.soap.wsdl-cache-ttl). У кеша в пам'яті також є максимальна кількість записів, що визначається параметром [soap.wsdl\_cache\_limit](soap.configuration.md#ini.soap.wsdl-cache-limit)

Якщо не вказано, використовуватиметься параметр конфігурації [soap.wsdl\_cache](soap.configuration.md#ini.soap.wsdl-cache)

`user_agent`string

Значение для использования в HTTP-заголовке`User-Agent` під час виконання запитів.

Можно также установить с помощью параметра[`stream_context`](soapclient.construct.md#soapclient.construct.options.stream-context)

Якщо не вказано, User-Agent буде `"PHP-SOAP/"` за яким слідує значення **`PHP_VERSION`**

`stream_context`resource

Контекст[stream context](context.md), створений за допомогою функції [stream\_context\_create()](function.stream-context-create.md), яка дає змогу встановити додаткові параметри.

Контекст може містити [параметри контексту сокету](context.socket.md) [параметри контексту SSL](context.ssl.md), а також вибрані [опції контексту HTTP](context.http.md) `content_type` `header` `max_redirects` `protocol_version`, и`user_agent`

Зверніть увагу, що наступні заголовки HTTP генеруються автоматично або на основі інших параметрів і будуть ігноруватися, якщо вказані в параметрі контексту `'header'` `host` `connection` `user-agent` `content-length` `content-type` `cookie` `authorization`и`proxy-authorization`

`features`int

Бітова маска для включення однієї або кількох таких функцій:

**`SOAP_SINGLE_ELEMENT_ARRAYS`**

При декодуванні відповіді масив за замовчуванням визначається, чи з'являється ім'я елемента один чи кілька разів у певному батьківському елементі. Для елементів, які з'являються лише один раз, властивість об'єкта дозволяє отримати прямий доступ до вмісту; для елементів, які з'являються більше одного разу, властивість містить масив із вмістом кожного відповідного елемента.

Якщо увімкнено функцію **`SOAP_SINGLE_ELEMENT_ARRAYS`**, елементи, які з'являються лише один раз, поміщаються в одноелементний масив, щоб доступ був послідовним для всіх елементів. Це буде працювати лише при використанні WSDL, що містить схему відповіді. Для демонстрації дивіться розділ із прикладами.

**`SOAP_USE_XSI_ARRAY_TYPE`**

Якщо [параметру`use`](soapclient.construct.md#soapclient.construct.options.use)или свойству WSDL передано значение`encoded`, масиви примусово використовують тип `SOAP-ENC:Array`, а чи не специфічний для схеми.

**`SOAP_WAIT_ONE_WAY_CALLS`**

Очікування відповіді, навіть якщо WSDL вказує на односторонній запит.

`keep_alive`bool

Логічне значення, що визначає, чи слід надсилати заголовок `Connection: Keep-Alive`или`Connection: close`

По умолчанию\*\*`true`\*\*

`ssl_method`string

Визначає версію протоколу SSL або TLS для використання у захищених з'єднаннях HTTP замість узгодження за промовчанням. Вказівка **`SOAP_SSL_METHOD_SSLv2`** або **`SOAP_SSL_METHOD_SSLv3`** змусить використовувати SSL 2 або SSL 3 відповідно. Вказівка ​​константи **`SOAP_SSL_METHOD_SSLv23`** немає сенсу; константа існує лише зворотної сумісності. Починаючи з PHP 7.2, вказівка ​​константи **`SOAP_SSL_METHOD_TLS`** також немає сенсу; у попередніх версіях константа визначала примусове використання TLS 1.0.

Зверніть увагу, що SSL версій 2 і 3 вважаються небезпечними і можуть не підтримуватись встановленою бібліотекою OpenSSL.

Параметр оголошено *Застарілим*починаючи з PHP 8.1.0. Більш гнучкою альтернативою, яка дозволяє вказувати окремі версії TLS, можна використовувати параметр [`stream_context`](soapclient.construct.md#soapclient.construct.options.stream-context) з параметром контексту 'crypto\_method'.

**Приклад #1 Вказівка ​​використання тільки TLS 1.3**

```php
<?php
$context = stream_context_create([
    'ssl' => [
        'crypto_method' => STREAM_CRYPTO_METHOD_TLSv1_3_CLIENT
     ]
]);
$client = new SoapClient("some.wsdl", ['context' => $context]);
```

### Помилки

Метод**SoapClient::\_\_construct()** виводить помилку рівня **`E_ERROR`**, якщо параметри `location`и`uri` не вказано у режимі не-WSDL.

Викидається виняток [SoapFault](class.soapfault.md), якщо параметр `wsdl` URI не може бути завантажено.

### Приклади

**Приклад #2 Приклад використання** SoapClient::\_\_construct()\*\*\*\*

```php
<?php

$client = new SoapClient("some.wsdl");

$client = new SoapClient("some.wsdl", array('soap_version'   => SOAP_1_2));

$client = new SoapClient("some.wsdl", array('login'          => "some_name",
                                            'password'       => "some_password"));

$client = new SoapClient("some.wsdl", array('proxy_host'     => "localhost",
                                            'proxy_port'     => 8080));

$client = new SoapClient("some.wsdl", array('proxy_host'     => "localhost",
                                            'proxy_port'     => 8080,
                                            'proxy_login'    => "some_name",
                                            'proxy_password' => "some_password"));

$client = new SoapClient("some.wsdl", array('local_cert'     => "cert_key.pem"));

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/"));

$client = new SoapClient(null, array('location' => "http://localhost/soap.php",
                                     'uri'      => "http://test-uri/",
                                     'style'    => SOAP_DOCUMENT,
                                     'use'      => SOAP_LITERAL));

$client = new SoapClient("some.wsdl",
  array('compression' => SOAP_COMPRESSION_ACCEPT | SOAP_COMPRESSION_GZIP | 9));

$client = new SoapClient("some.wsdl", array('encoding'=>'ISO-8859-1'));

class MyBook {
    public $title;
    public $author;
}

$client = new SoapClient("books.wsdl", array('classmap' => array('book' => "MyBook")));

$typemap = array(
    array("type_ns"  => "http://schemas.example.com",
         "type_name" => "book",
         "from_xml"  => "unserialize_book",
         "to_xml"    => "serialize_book")
);
$client = new SoapClient("books.wsdl", array('typemap' => $typemap));

?>
```

**Приклад #3 Приклад використання** `SOAP_SINGLE_ELEMENT_ARRAYS`\*\*\*\*

```php
/* Предполагая, что ответ, подобный этому, и соответствующий WSDL:
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns="urn:example">
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

echo "По умолчанию:\n";

$client = new TestSoapClient(__DIR__ . '/temp.wsdl');
$response = $client->exampleRequest();
var_dump( $response->collection[0]->item );
var_dump( $response->collection[1]->item );

echo "\nС помощью SOAP_SINGLE_ELEMENT_ARRAYS:\n";

$client = new TestSoapClient(__DIR__ . '/temp.wsdl', ['features' => SOAP_SINGLE_ELEMENT_ARRAYS]);
$response = $client->exampleRequest();
var_dump( $response->collection[0]->item );
var_dump( $response->collection[1]->item );
```

Результат виконання наведеного прикладу:

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
