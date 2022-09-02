---
navigation:
  - yaf-response-abstract.destruct.md: '« YafResponseAbstract::destruct'
  - yaf-response-abstract.getheader.md: 'YafResponseAbstract::getHeader »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: YafResponseAbstract
title: 'YafResponseAbstract::getBody'
---
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

Ключ вмісту, якщо ви не вкажете, використовуватиметься YafResponseAbstract::DEFAULTBODY. Якщо ви передасте \*\*`null`\*\*тоді весь вміст буде повернуто як масив

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

-   [YafResponseAbstract::setBody()](yaf-response-abstract.setbody.md) - Встановлює вміст відповіді
-   [YafResponseAbstract::appendBody()](yaf-response-abstract.appendbody.md) - Додає вміст до тіла відповіді
-   [YafResponseAbstract::prependBody()](yaf-response-abstract.prependbody.md) - Призначення prependBody
-   [YafResponseAbstract::clearBody()](yaf-response-abstract.clearbody.md) - скидає все існуюче тіло відповіді
