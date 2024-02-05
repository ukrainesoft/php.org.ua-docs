---
navigation:
  - class.yaf-response-abstract.md: « Yaf\_Response\_Abstract
  - yaf-response-abstract.clearbody.md: 'Yaf\_Response\_Abstract::clearBody »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: Yaf\_Response\_Abstract
title: 'Yaf\_Response\_Abstract::appendBody'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Response\_Abstract::appendBody

(Yaf >=1.0.0)

Yaf\_Response\_Abstract::appendBody — Додає вміст до тіла відповіді

### Опис

```methodsynopsis
public Yaf_Response_Abstract::appendBody(string $content, string $key = ?): bool
```

Додає вміст до існуючого блоку вмісту

### Список параметрів

`body`

Рядок вмісту

`key`

Ключ контенту, ви можете встановити контент з ключем, якщо ви не вкажете, буде використовуватися Yaf\_Response\_Abstract::DEFAULT\_BODY

> **Зауваження** :
> 
> Параметр додано з 2.2.0

### Значення, що повертаються

bool

### Приклади

**Пример #1 Пример использования**Yaf\_Response\_Abstract::appendBody()\*\*\*\*

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->prependBody(", Мир");

echo $response;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Привет, Мир
```

### Дивіться також

-   [Yaf\_Config\_Ini](class.yaf-config-ini.md)
-   [Yaf\_Response\_Abstract::getBody()](yaf-response-abstract.getbody.md) \- Отримує наявний вміст
-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.md) \- Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::prependBody()](yaf-response-abstract.prependbody.md) \- Призначення prependBody
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.md) \- скидає все існуюче тіло відповіді
