Додає вміст до тіла відповіді

-   [« Yaf\_Response\_Abstract](class.yaf-response-abstract.html)
    
-   [Yaf\_Response\_Abstract::clearBody »](yaf-response-abstract.clearbody.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Response\_Abstract](class.yaf-response-abstract.html)
    
-   Додає вміст до тіла відповіді
    

# YafResponseAbstract::appendBody

(Yaf >=1.0.0)

YafResponseAbstract::appendBody — Додає вміст до тіла відповіді

### Опис

```methodsynopsis
public Yaf_Response_Abstract::appendBody(string $content, string $key = ?): bool
```

Додає вміст до існуючого блоку вмісту

### Список параметрів

`body`

Рядок вмісту

`key`

Ключ контенту, ви можете встановити контент з ключем, якщо ви не вкажете, буде використовуватися YafResponseAbstract::DEFAULTBODY

> **Зауваження**
> 
> Параметр додано з 2.2.0

### Значення, що повертаються

bool

### Приклади

**Приклад #1 Приклад використання **YafResponseAbstract::appendBody()****

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->prependBody(", Мир");

echo $response;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Привет, Мир
```

### Дивіться також

-   [Yaf\_Config\_Ini](class.yaf-config-ini.html)
-   [Yaf\_Response\_Abstract::getBody()](yaf-response-abstract.getbody.html) - Отримує наявний вміст
-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.html) - Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::prependBody()](yaf-response-abstract.prependbody.html) - Призначення prependBody
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.html) - скидає все існуюче тіло відповіді