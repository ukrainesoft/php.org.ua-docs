Встановлює вміст відповіді

-   [« Yaf\_Response\_Abstract::setAllHeaders](yaf-response-abstract.setallheaders.html)
    
-   [Yaf\_Response\_Abstract::setHeader »](yaf-response-abstract.setheader.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Response\_Abstract](class.yaf-response-abstract.html)
    
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

-   [Yaf\_Response\_Abstract::getBody()](yaf-response-abstract.getbody.html) - Отримує наявний вміст
-   [Yaf\_Response\_Abstract::appendBody()](yaf-response-abstract.appendbody.html) - Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::prependBody()](yaf-response-abstract.prependbody.html) - Призначення prependBody
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.html) - скидає все існуюче тіло відповіді