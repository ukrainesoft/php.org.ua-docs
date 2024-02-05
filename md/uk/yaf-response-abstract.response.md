---
navigation:
  - yaf-response-abstract.prependbody.md: '« Yaf\_Response\_Abstract::prependBody'
  - yaf-response-abstract.setallheaders.md: 'Yaf\_Response\_Abstract::setAllHeaders »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: Yaf\_Response\_Abstract
title: 'Yaf\_Response\_Abstract::response'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Response\_Abstract::response

(Yaf >=1.0.0)

Yaf\_Response\_Abstract::response — Надсилає відповідь

### Опис

```methodsynopsis
public Yaf_Response_Abstract::response(): void
```

Відправляє відповідь

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Response\_Abstract::response()\*\*\*\*

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->setBody(", Мир", "footer");

$response->response();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Привет, Мир
```

### Дивіться також

-   [Yaf\_Response\_Abstract::setBody()](yaf-response-abstract.setbody.md) \- Встановлює вміст відповіді
-   [Yaf\_Response\_Abstract::clearBody()](yaf-response-abstract.clearbody.md) \- скидає все існуюче тіло відповіді
