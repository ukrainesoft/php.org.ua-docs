---
navigation:
  - yaf-response-abstract.getheader.md: '« Yaf\_Response\_Abstract::getHeader'
  - yaf-response-abstract.response.md: 'Yaf\_Response\_Abstract::response »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: Yaf\_Response\_Abstract
title: 'Yaf\_Response\_Abstract::prependBody'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Response\_Abstract::prependBody

(Yaf >=1.0.0)

Yaf\_Response\_Abstract::prependBody — Призначення prependBody

### Опис

```methodsynopsis
public Yaf_Response_Abstract::prependBody(string $content, string $key = ?): bool
```

Додає вміст до існуючого блоку вмісту

### Список параметрів

`body`

Рядок вмісту

`key`

Ключ вмісту, ви можете встановити вміст із ключем, якщо ви не вкажете, то буде використовуватися Yaf\_Response\_Abstract::DEFAULT\_BODY

> **Зауваження** :
> 
> Параметр додано з 2.2.0

### Значення, що повертаються

bool

### Приклади

**Приклад #1 Приклад використання** Yaf\_Response\_Abstract::prependBody()\*\*\*\*

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Мир")->prependBody("Привет ,");

echo $response;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Привет, Мир
```

### Дивіться також

-   [Yaf\_Response\_Abstract::getBody()](yaf-response-abstract.getbody.md) \- Отримує наявний вміст
-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.md) \- Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::appendBody()](yaf-response-abstract.appendbody.md) \- Додає вміст до тіла відповіді
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.md) \- скидає все існуюче тіло відповіді
