Призначення prependBody

-   [« Yaf\_Response\_Abstract::getHeader](yaf-response-abstract.getheader.html)
    
-   [Yaf\_Response\_Abstract::response »](yaf-response-abstract.response.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Response\_Abstract](class.yaf-response-abstract.html)
    
-   Призначення prependBody
    

# YafResponseAbstract::prependBody

(Yaf >=1.0.0)

YafResponseAbstract::prependBody — Призначення prependBody

### Опис

```methodsynopsis
public Yaf_Response_Abstract::prependBody(string $content, string $key = ?): bool
```

Додає вміст до існуючого блоку вмісту

### Список параметрів

`body`

Рядок вмісту

`key`

Ключ вмісту, ви можете встановити вміст із ключем, якщо ви не вкажете, то буде використовуватися YafResponseAbstract::DEFAULTBODY

> **Зауваження**
> 
> Параметр додано з 2.2.0

### Значення, що повертаються

bool

### Приклади

**Приклад #1 Приклад використання **YafResponseAbstract::prependBody()****

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Мир")->prependBody("Привет ,");

echo $response;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Привет, Мир
```

### Дивіться також

-   [Yaf\_Response\_Abstract::getBody()](yaf-response-abstract.getbody.html) - Отримує наявний вміст
-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.html) - Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::appendBody()](yaf-response-abstract.appendbody.html) - Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.html) - скидає все існуюче тіло відповіді