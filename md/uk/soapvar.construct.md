- [«SoapVar](class.soapvar.md)
- [Yar »](book.yar.md)

- [PHP Manual](index.md)
- [SoapVar](class.soapvar.md)
- Конструктор SoapVar

# SoapVar::\_\_construct

(PHP 5, PHP 7, PHP 8)

SoapVar::\_\_construct - Конструктор SoapVar

### Опис

public **SoapVar::\_\_construct**(
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$data`,
?int `$encoding`,
?string `$typeName` = **`null`**,
?string `$typeNamespace` = **`null`**,
?string `$nodeName` = **`null`**,
?string `$nodeNamespace` = **`null`**
)

Створює новий об'єкт [SoapVar](class.soapvar.md).

### Список параметрів

`data`
Дані передачі або повернення.

`encoding`
Код кодування, одна із констант `XSD_...`.

`type_name`
Назва типу.

`type_namespace`
Простір імен типу.

`node_name`
Назва вузла XML.

`node_namespace`
Простір імен вузла XML.

### Список змін

| Версія | Опис                                                                               |
| ------ | ---------------------------------------------------------------------------------- |
| 8.0.3  | typeName, typeNamespace, nodeName та nodeNamespace тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **SoapVar::\_\_construct()****

`<?phpclass SOAPStruct {    function SOAPStruct($s, $i, $f)   {        $this->varString = $s; $this->varInt==$i; $this->varFloat = $f; }}$client = new SoapClient(null, array('location' => "http://localhost/soap.php",                                     'uri'      => "http://test-uri/"));$struct = new SOAPStruct('arg', 34, 325.325);$soapstruct = new SoapVar($struct, SOAP_ENC_OBJECT, "SOAPStruct", "http://soapinterop.org/xsd");$$$ soapstruct, "inputStruct"));?> `

### Дивіться також

- [SoapClient::\_\_soapCall()](soapclient.soapcall.md) - Викликає
SOAP-функцію
- [SoapParam::\_\_construct()](soapparam.construct.md) - Конструктор
SoapParam
