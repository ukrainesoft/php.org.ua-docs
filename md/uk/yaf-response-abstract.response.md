Відправляє відповідь

-   [« YafResponseAbstract::prependBody](yaf-response-abstract.prependbody.html)
    
-   [YafResponseAbstract::setAllHeaders »](yaf-response-abstract.setallheaders.html)
    
-   [PHP Manual](index.md)
    
-   [YafResponseAbstract](class.yaf-response-abstract.html)
    
-   Відправляє відповідь
    

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

-   [YafResponseAbstract::setBody()](yaf-response-abstract.setbody.html) - Встановлює вміст відповіді
-   [YafResponseAbstract::clearBody()](yaf-response-abstract.clearbody.html) - скидає все існуюче тіло відповіді