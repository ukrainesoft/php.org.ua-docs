---
navigation:
  - yaf-response-abstract.setallheaders.md: '« Yaf\_Response\_Abstract::setAllHeaders'
  - yaf-response-abstract.setheader.md: 'Yaf\_Response\_Abstract::setHeader »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: Yaf\_Response\_Abstract
title: 'Yaf\_Response\_Abstract::setBody'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Response\_Abstract::setBody

(Yaf >=1.0.0)

Yaf\_Response\_Abstract::setBody — Встановлює вміст відповіді

### Опис

```methodsynopsis
public Yaf_Response_Abstract::setBody(string $content, string $key = ?): bool
```

Встановлює вміст відповіді

### Список параметрів

`body`

Рядок вмісту

`key`

Ключ вмісту, ви можете встановити вміст із ключем, якщо ви не вкажете, то буде використовуватися Yaf\_Response\_Abstract::DEFAULT\_BODY

> **Зауваження** :
> 
> Параметр додано з 2.2.0

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Response\_Abstract::setBody()\*\*\*\*

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->setBody(", Мир", "footer");

print_r($response);
echo $response;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Yaf_Response_Http Object
(
    [_header:protected] => Array
        (
        )

    [_body:protected] => Array
        (
            [content] => Привет
            [footer] => , Мир
        )

    [_sendheader:protected] => 1
    [_response_code:protected] => 200
)
Привет, Мир
```

### Дивіться також

-   [Yaf\_Response\_Abstract::getBody()](yaf-response-abstract.getbody.md) \- Отримує наявний вміст
-   [Yaf\_Response\_Abstract::appendBody()](yaf-response-abstract.appendbody.md) \- Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::prependBody()](yaf-response-abstract.prependbody.md) \- Призначення prependBody
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.md) \- скидає все існуюче тіло відповіді
