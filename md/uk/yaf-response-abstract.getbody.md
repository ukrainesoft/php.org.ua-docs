Отримує існуючий вміст

-   [« Yaf\_Response\_Abstract::\_\_destruct](yaf-response-abstract.destruct.html)
    
-   [Yaf\_Response\_Abstract::getHeader »](yaf-response-abstract.getheader.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Response\_Abstract](class.yaf-response-abstract.html)
    
-   Отримує існуючий вміст
    

# YafResponseAbstract::getBody

(Yaf >=1.0.0)

YafResponseAbstract::getBody — Отримує існуючий вміст

### Опис

```methodsynopsis
public Yaf_Response_Abstract::getBody(string $key = ?): mixed
```

Отримує існуючий вміст

### Список параметрів

`key`

Ключ вмісту, якщо ви не вкажете, використовуватиметься YafResponseAbstract::DEFAULTBODY. Якщо ви передасте **`null`**тоді весь вміст буде повернуто як масив

> **Зауваження**
> 
> Параметр було додано з 2.2.0

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafResponseAbstract::getBody()****

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->setBody(", Мир", "footer");

var_dump($response->getBody()); //по умолчанию
var_dump($response->getBody(Yaf_Response_Abstract::DEFAULT_BODY)); //так же, как и выше
var_dump($response->getBody("footer"));
var_dump($response->getBody(NULL)); //получить все
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "Привет"
string(5) "Привет"
string(6) ", Мир"
array(2) {
  ["content"]=>
  string(5) "Привет"
  ["footer"]=>
  string(6) ", Мир"
}
```

### Дивіться також

-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.html) - Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::appendBody()](yaf-response-abstract.appendbody.html) - Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::prependBody()](yaf-response-abstract.prependbody.html) - Призначення prependBody
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.html) - скидає все існуюче тіло відповіді