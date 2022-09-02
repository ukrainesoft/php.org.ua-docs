---
navigation:
  - yaf-response-abstract.prependbody.md: '« YafResponseAbstract::prependBody'
  - yaf-response-abstract.setallheaders.md: 'YafResponseAbstract::setAllHeaders »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: YafResponseAbstract
title: 'YafResponseAbstract::response'
---
# YafResponseAbstract::response

(Yaf >=1.0.0)

YafResponseAbstract::response — Надсилає відповідь

### Опис

```methodsynopsis
public Yaf_Response_Abstract::response(): void
```

Відправляє відповідь

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafResponseAbstract::response()****

```php
<?php
$response = new Yaf_Response_Http();

$response->setBody("Привет")->setBody(", Мир", "footer");

$response->response();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Привет, Мир
```

### Дивіться також

-   [YafResponseAbstract::setBody()](yaf-response-abstract.setbody.md) - Встановлює вміст відповіді
-   [YafResponseAbstract::clearBody()](yaf-response-abstract.clearbody.md) - скидає все існуюче тіло відповіді
