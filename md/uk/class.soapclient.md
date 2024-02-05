---
navigation:
  - function.use-soap-error-handler.md: « use\_soap\_error\_handler
  - soapclient.call.md: 'SoapClient::\_\_call »'
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: 'Класс[SoapClient](class.soapclient.md)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Класс[SoapClient](class.soapclient.md)

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс SoapClient представляет собой клиента для серверов[» SOAP 1.1](http://www.w3.org/TR/soap11/) [» SOAP 1.2](http://www.w3.org/TR/soap12/). Він може використовуватися в режимі WSDL або без нього.

## Огляд класів

```classsynopsis

    
     class SoapClient
     {

    /* Свойства */
    
     private
     ?string
      $uri = null;

    private
     ?int
      $style = null;

    private
     ?int
      $use = null;

    private
     ?string
      $location = null;

    private
     bool
      $trace = false;

    private
     ?int
      $compression = null;

    private
     ?resource
      $sdl = null;

    private
     ?resource
      $typemap = null;

    private
     ?resource
      $httpsocket = null;

    private
     ?resource
      $httpurl = null;

    private
     ?string
      $_login = null;

    private
     ?string
      $_password = null;

    private
     bool
      $_use_digest = false;

    private
     ?string
      $_digest = null;

    private
     ?string
      $_proxy_host = null;

    private
     ?int
      $_proxy_port = null;

    private
     ?string
      $_proxy_login = null;

    private
     ?string
      $_proxy_password = null;

    private
     bool
      $_exceptions = true;

    private
     ?string
      $_encoding = null;

    private
     ?array
      $_classmap = null;

    private
     ?int
      $_features = null;

    private
     int
      $_connection_timeout;

    private
     ?resource
      $_stream_context = null;

    private
     ?string
      $_user_agent = null;

    private
     bool
      $_keep_alive = true;

    private
     ?int
      $_ssl_method = null;

    private
     int
      $_soap_version;

    private
     ?int
      $_use_proxy = null;

    private
     array
      $_cookies = [];

    private
     ?array
      $__default_headers = null;

    private
     ?SoapFault
      $__soap_fault = null;

    private
     ?string
      $__last_request = null;

    private
     ?string
      $__last_response = null;

    private
     ?string
      $__last_request_headers = null;

    private
     ?string
      $__last_response_headers = null;


    /* Методы */
    
   public __construct(?string $wsdl, array $options = [])

    public __call(string $name, array $args): mixed
public __doRequest(    string $request,    string $location,    string $action,    int $version,    bool $oneWay = false): ?string
public __getCookies(): array
public __getFunctions(): ?array
public __getLastRequest(): ?string
public __getLastRequestHeaders(): ?string
public __getLastResponse(): ?string
public __getLastResponseHeaders(): ?string
public __getTypes(): ?array
public __setCookie(string $name, ?string $value = null): void
public __setLocation(?string $location = null): ?string
public __setSoapHeaders(SoapHeader|array|null $headers = null): bool
public __soapCall(    string $name,    array $args,    ?array $options = null,    SoapHeader|array|null $inputHeaders = null,    array &$outputHeaders = null): mixed

   }
```

## Властивості

\_\_default\_headers

\_\_last\_request

\_\_last\_request\_headers

\_\_last\_response

\_\_last\_response\_headers

\_\_soap\_fault

\_classmap

\_connection\_timeout

\_cookies

\_digest

\_encoding

\_exceptions

\_features

\_keep\_alive

\_login

\_password

\_proxy\_host

\_proxy\_login

\_proxy\_password

\_proxy\_port

\_soap\_version

\_ssl\_method

\_stream\_context

\_use\_digest

\_use\_proxy

\_user\_agent

compression

httpsocket

httpurl

location

sdl

style

trace

typemap

uri

use

## Зміст

-   [SoapClient::\_\_call](soapclient.call.md) \- Викликає SOAP-функцію (застарілий метод)
-   [SoapClient::\_\_construct](soapclient.construct.md) \- Конструктор класу SoapClient
-   [SoapClient::\_\_doRequest](soapclient.dorequest.md) \- Виконує SOAP-запит
-   [SoapClient::\_\_getCookies](soapclient.getcookies.md)— Отримати список cookies
-   [SoapClient::\_\_getFunctions](soapclient.getfunctions.md)— Повертає список доступних SOAP-функцій
-   [SoapClient::\_\_getLastRequest](soapclient.getlastrequest.md) \- Повертає останній SOAP-запит
-   [SoapClient::\_\_getLastRequestHeaders](soapclient.getlastrequestheaders.md)— Повертає SOAP-заголовки останнього запиту
-   [SoapClient::\_\_getLastResponse](soapclient.getlastresponse.md)— Повертає останню SOAP-відповідь
-   [SoapClient::\_\_getLastResponseHeaders](soapclient.getlastresponseheaders.md)— Повертає SOAP-заголовки останньої відповіді
-   [SoapClient::\_\_getTypes](soapclient.gettypes.md)— Повертає список типів SOAP
-   [SoapClient::\_\_setCookie](soapclient.setcookie.md)— Встановлює cookie для запитів SOAP
-   [SoapClient::\_\_setLocation](soapclient.setlocation.md)— Встановлює адресу веб-служби, що використовується.
-   [SoapClient::\_\_setSoapHeaders](soapclient.setsoapheaders.md)— Встановлює заголовки SOAP для наступних дзвінків
-   [SoapClient::\_\_soapCall](soapclient.soapcall.md) \- Викликає SOAP-функцію
