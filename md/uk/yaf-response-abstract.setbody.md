- [« Yaf_Response_Abstract::setAllHeaders](yaf-response-abstract.setallheaders.md)
- [Yaf_Response_Abstract::setHeader »](yaf-response-abstract.setheader.md)

- [PHP Manual](index.md)
- [Yaf_Response_Abstract](class.yaf-response-abstract.md)
- Встановлює вміст відповіді

# Yaf_Response_Abstract::setBody

(Yaf \>=1.0.0)

Yaf_Response_Abstract::setBody — Встановлює вміст відповіді

### Опис

public **Yaf_Response_Abstract::setBody**(string `$content`, string
`$key` = ?): bool

Встановлює вміст відповіді

### Список параметрів

`body`
Рядок вмісту

`key`
Ключ вмісту, ви можете встановити вміст із ключем, якщо ви не
вкажете, то використовуватиметься Yaf_Response_Abstract::DEFAULT_BODY

> **Примітка**:
>
> Параметр додано з 2.2.0

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **Yaf_Response_Abstract::setBody()****

` <?php$response = new Yaf_Response_Http();$response->setBody("Привіт")->setBody(", Світ", "footer");print_r($response);echo $response;?> `

Результатом виконання цього прикладу буде щось подібне:

Yaf_Response_Http Object
(
[_header:protected] => Array
(
)

[_body:protected] => Array
(
[content] => Привіт
[footer] => , Світ
)

[_sendheader:protected] => 1
[_response_code:protected] => 200
)
Привіт світ

### Дивіться також

- [Yaf_Response_Abstract::getBody()](yaf-response-abstract.getbody.md) -
Отримує існуючий вміст
- [Yaf_Response_Abstract::appendBody()](yaf-response-abstract.appendbody.md) -
Додає вміст до тіла відповіді
- [Yaf_Response_Abstract::prependBody()](yaf-response-abstract.prependbody.md) -
Призначення prependBody
- [Yaf_Response_Abstract::clearBody()](yaf-response-abstract.clearbody.md) -
Скидає все існуюче тіло відповіді
