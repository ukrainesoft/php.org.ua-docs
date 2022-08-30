Встановлює вміст відповіді

-   [« YafResponseAbstract::setAllHeaders](yaf-response-abstract.setallheaders.html)
    
-   [YafResponseAbstract::setHeader »](yaf-response-abstract.setheader.html)
    
-   [PHP Manual](index.html)
    
-   [YafResponseAbstract](class.yaf-response-abstract.html)
    
-   Встановлює вміст відповіді
    

# YafResponseAbstract::setBody

(Yaf >=1.0.0)

YafResponseAbstract::setBody — Встановлює вміст відповіді

### Опис

```methodsynopsis
public Yaf_Response_Abstract::setBody(string $content, string $key = ?): bool
```

Встановлює вміст відповіді

### Список параметрів

`body`

Рядок вмісту

`key`

Ключ вмісту, ви можете встановити вміст із ключем, якщо ви не вкажете, то буде використовуватися YafResponseAbstract::DEFAULTBODY

> **Зауваження**
> 
> Параметр додано з 2.2.0

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafResponseAbstract::setBody()****

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->setBody(", Мир", "footer");

print_r($response);
echo $response;
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [YafResponseAbstract::getBody()](yaf-response-abstract.getbody.html) - Отримує наявний вміст
-   [YafResponseAbstract::appendBody()](yaf-response-abstract.appendbody.html) - Додає вміст до тіла відповіді
-   [YafResponseAbstract::prependBody()](yaf-response-abstract.prependbody.html) - Призначення prependBody
-   [YafResponseAbstract::clearBody()](yaf-response-abstract.clearbody.html) - скидає все існуюче тіло відповіді