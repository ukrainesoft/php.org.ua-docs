---
navigation:
  - class.yaf-response-abstract.md: « YafResponseAbstract
  - yaf-response-abstract.clearbody.md: 'YafResponseAbstract::clearBody »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: YafResponseAbstract
title: 'YafResponseAbstract::appendBody'
---
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

-   [YafConfigIni](class.yaf-config-ini.md)
-   [YafResponseAbstract::getBody()](yaf-response-abstract.getbody.md) - Отримує наявний вміст
-   [YafResponseAbstract::setBody()](yaf-response-abstract.setbody.md) - Встановлює вміст відповіді
-   [YafResponseAbstract::prependBody()](yaf-response-abstract.prependbody.md) - Призначення prependBody
-   [YafResponseAbstract::clearBody()](yaf-response-abstract.clearbody.md) - скидає все існуюче тіло відповіді
