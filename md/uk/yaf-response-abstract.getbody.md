---
navigation:
  - yaf-response-abstract.destruct.md: '« Yaf\_Response\_Abstract::\_\_destruct'
  - yaf-response-abstract.getheader.md: 'Yaf\_Response\_Abstract::getHeader »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: Yaf\_Response\_Abstract
title: 'Yaf\_Response\_Abstract::getBody'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Response\_Abstract::getBody

(Yaf >=1.0.0)

Yaf\_Response\_Abstract::getBody — Отримує існуючий вміст

### Опис

```methodsynopsis
public Yaf_Response_Abstract::getBody(string $key = ?): mixed
```

Отримує існуючий вміст

### Список параметрів

`key`

Ключ вмісту, якщо ви не вкажете, використовуватиметься Yaf\_Response\_Abstract::DEFAULT\_BODY. Якщо ви передасте \*\*`null`\*\*тоді весь вміст буде повернуто як масив

> **Зауваження** :
> 
> Параметр було додано з 2.2.0

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Response\_Abstract::getBody()\*\*\*\*

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->setBody(", Мир", "footer");

var_dump($response->getBody()); //по умолчанию
var_dump($response->getBody(Yaf_Response_Abstract::DEFAULT_BODY)); //так же, как и выше
var_dump($response->getBody("footer"));
var_dump($response->getBody(NULL)); //получить все
?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.md) \- Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::appendBody()](yaf-response-abstract.appendbody.md) \- Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::prependBody()](yaf-response-abstract.prependbody.md) \- Призначення prependBody
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.md) \- скидає все існуюче тіло відповіді
