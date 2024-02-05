---
navigation:
  - soap.resources.md: « Типи ресурсів
  - ref.soap.md: Функції SOAP »
  - index.md: PHP Manual
  - book.soap.md: SOAP
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**Константи SOAP**

| Константа | Значение | Опис |
| --- | --- | --- |
| **`SOAP_1_1`**(int) |  | Визначає використання SOAP 1.1 при передачі як параметр `soap_version` методом [SoapServer::\_\_construct()](soapserver.construct.md) або [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_1_2`**(int) |  | Визначає використання SOAP 1.2 при передачі як параметр `soap_version` методом [SoapServer::\_\_construct()](soapserver.construct.md) або [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_PERSISTENCE_SESSION`**(int) |  |  |
| **`SOAP_PERSISTENCE_REQUEST`**(int) |  |  |
| **`SOAP_FUNCTIONS_ALL`**(int) | 999 |  |
| **`SOAP_ENCODED`**(int) |  | Визначає використання кодування SOAP при передачі як параметр `use` методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_LITERAL`**(int) |  | Визначає використання специфічного для сервісу кодування при передачі як параметр `use` методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_RPC`**(int) |  | Визначає використання прив'язки в стилі RPC при передачі як параметр `style` методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_DOCUMENT`**(int) |  | Визначає використання прив'язки до документа при передачі як параметр `style` методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_ACTOR_NEXT`**(int) |  |  |
| **`SOAP_ACTOR_NONE`**(int) |  |  |
| **`SOAP_ACTOR_UNLIMATERECEIVER`**(int) | 3 |  |
| **`SOAP_COMPRESSION_ACCEPT`**(int) | 32 | Визначає використання заголовка "Accept-Encoding" під час передачі [параметра `compression`](soapclient.construct.md#soapclient.construct.options.compression) методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_COMPRESSION_GZIP`**(int) |  | Визначає використання стиснення gzip під час передачі [параметра `compression`](soapclient.construct.md#soapclient.construct.options.compression) методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_COMPRESSION_DEFLATE`**(int) | 16 | Визначає використання стиснення deflate при передачі [параметра `compression`](soapclient.construct.md#soapclient.construct.options.compression) методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_AUTHENTICATION_BASIC`**(int) |  | Визначає використання базової аутентифікації HTTP під час передачі параметра `authentication` методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_AUTHENTICATION_DIGEST`**(int) |  | Визначає використання аутентифікації HTTP Digest Authentication під час передачі параметра `authentication` методом [SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_SSL_METHOD_TLS`**(int) |  | Використовується із застарілим [параметром `ssl_method`](soapclient.construct.md#soapclient.construct.options.ssl-method)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_SSL_METHOD_SSLv2`**(int) |  | Використовується із застарілим [параметром `ssl_method`](soapclient.construct.md#soapclient.construct.options.ssl-method)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_SSL_METHOD_SSLv3`**(int) |  | Використовується із застарілим [параметром `ssl_method`](soapclient.construct.md#soapclient.construct.options.ssl-method)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_SSL_METHOD_SSLv23`**(int) | 3 | Використовується із застарілим [параметром `ssl_method`](soapclient.construct.md#soapclient.construct.options.ssl-method)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`UNKNOWN_TYPE`**(int) | 999998 |  |
| **`XSD_STRING`**(int) | 101 |  |
| **`XSD_BOOLEAN`**(int) | 102 |  |
| **`XSD_DECIMAL`**(int) | 103 |  |
| **`XSD_FLOAT`**(int) | 104 |  |
| **`XSD_DOUBLE`**(int) | 105 |  |
| **`XSD_DURATION`**(int) | 106 |  |
| **`XSD_DATETIME`**(int) | 107 |  |
| **`XSD_TIME`**(int) | 108 |  |
| **`XSD_DATE`**(int) | 109 |  |
| **`XSD_GYEARMONTH`**(int) | 110 |  |
| **`XSD_GYEAR`**(int) | 111 |  |
| **`XSD_GMONTHDAY`**(int) | 112 |  |
| **`XSD_GDAY`**(int) | 113 |  |
| **`XSD_GMONTH`**(int) | 114 |  |
| **`XSD_HEXBINARY`**(int) | 115 |  |
| **`XSD_BASE64BINARY`**(int) | 116 |  |
| **`XSD_ANYURI`**(int) | 117 |  |
| **`XSD_QNAME`**(int) | 118 |  |
| **`XSD_NOTATION`**(int) | 119 |  |
| **`XSD_NORMALIZEDSTRING`**(int) | 120 |  |
| **`XSD_TOKEN`**(int) | 121 |  |
| **`XSD_LANGUAGE`**(int) | 122 |  |
| **`XSD_NMTOKEN`**(int) | 123 |  |
| **`XSD_NAME`**(int) | 124 |  |
| **`XSD_NCNAME`**(int) | 125 |  |
| **`XSD_ID`**(int) | 126 |  |
| **`XSD_IDREF`**(int) | 127 |  |
| **`XSD_IDREFS`**(int) | 128 |  |
| **`XSD_ENTITY`**(int) | 129 |  |
| **`XSD_ENTITIES`**(int) | 130 |  |
| **`XSD_INTEGER`**(int) | 131 |  |
| **`XSD_NONPOSITIVEINTEGER`**(int) | 132 |  |
| **`XSD_NEGATIVEINTEGER`**(int) | 133 |  |
| **`XSD_LONG`**(int) | 134 |  |
| **`XSD_INT`**(int) | 135 |  |
| **`XSD_SHORT`**(int) | 136 |  |
| **`XSD_BYTE`**(int) | 137 |  |
| **`XSD_NONNEGATIVEINTEGER`**(int) | 138 |  |
| **`XSD_UNSIGNEDLONG`**(int) | 139 |  |
| **`XSD_UNSIGNEDINT`**(int) | 140 |  |
| **`XSD_UNSIGNEDSHORT`**(int) | 141 |  |
| **`XSD_UNSIGNEDBYTE`**(int) | 142 |  |
| **`XSD_POSITIVEINTEGER`**(int) | 143 |  |
| **`XSD_NMTOKENS`**(int) | 144 |  |
| **`XSD_ANYTYPE`**(int) | 145 |  |
| **`XSD_ANYXML`**(int) | 147 |  |
| **`APACHE_MAP`**(int) | 200 |  |
| **`SOAP_ENC_OBJECT`**(int) | 301 |  |
| **`SOAP_ENC_ARRAY`**(int) | 300 |  |
| **`XSD_1999_TIMEINSTANT`**(int) | 401 |  |
| **`XSD_NAMESPACE`**(string) | [http://www.w3.org/2001/XMLSchema](http://www.w3.org/2001/XMLSchema) |  |
| **`XSD_1999_NAMESPACE`**(string) | [http://www.w3.org/1999/XMLSchema](http://www.w3.org/1999/XMLSchema) |  |
| **`SOAP_SINGLE_ELEMENT_ARRAYS`**(int) |  | Використовується з [параметром `features`](soapclient.construct.md#soapclient.construct.options.features)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_WAIT_ONE_WAY_CALLS`**(int) |  | Використовується з [параметром `features`](soapclient.construct.md#soapclient.construct.options.features)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`SOAP_USE_XSI_ARRAY_TYPE`**(int) | 4 | Використовується з [параметром `features`](soapclient.construct.md#soapclient.construct.options.features)метода[SoapClient::\_\_construct()](soapclient.construct.md) |
| **`WSDL_CACHE_NONE`**(int) |  | Вимикає кеш WSDL під час використання параметра [soap.wsdl\_cache](soap.configuration.md#ini.soap.wsdl-cache) або параметром `wsdl_cache` методів [SoapClient::\_\_construct()](soapclient.construct.md) і [SoapServer::\_\_construct()](soapserver.construct.md) |
| **`WSDL_CACHE_DISK`**(int) |  | Визначає використання кешу WSDL на диску лише за умови використання з параметром [soap.wsdl\_cache](soap.configuration.md#ini.soap.wsdl-cache) або параметром `wsdl_cache` методів [SoapClient::\_\_construct()](soapclient.construct.md) і [SoapServer::\_\_construct()](soapserver.construct.md) |
| **`WSDL_CACHE_MEMORY`**(int) |  | Визначає використання кешу WSDL у пам'яті лише при використанні з параметром [soap.wsdl\_cache](soap.configuration.md#ini.soap.wsdl-cache) або параметром `wsdl_cache` методів [SoapClient::\_\_construct()](soapclient.construct.md) і [SoapServer::\_\_construct()](soapserver.construct.md) |
| **`WSDL_CACHE_BOTH`**(int) | 3 | Визначає використання кешу WSDL як на диску, так і в пам'яті лише при використанні параметра [soap.wsdl\_cache](soap.configuration.md#ini.soap.wsdl-cache) або параметром `wsdl_cache` методів [SoapClient::\_\_construct()](soapclient.construct.md) і [SoapServer::\_\_construct()](soapserver.construct.md) |
