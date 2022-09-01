---
navigation:
  - class.yaf-dispatcher.html: « YafDispatcher
  - yaf-dispatcher.catchexception.html: 'YafDispatcher::catchException »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.html: YafDispatcher
title: 'YafDispatcher::autoRender'
---
# YafDispatcher::autoRender

(Yaf >=1.0.0)

YafDispatcher::autoRender — Включає/вимикає авторендеринг

### Опис

```methodsynopsis
public Yaf_Dispatcher::autoRender(bool $flag = ?): Yaf_Dispatcher
```

[YafDispatcher](class.yaf-dispatcher.html) буде відображатися автоматично після надсилання вхідного запиту. Ви можете запобігти рендерингу, викликавши цей метод за допомогою `flag` **`true`**

> **Зауваження**
> 
> Ви можете просто повернути **`false`** у дії, щоб запобігти автоматичному рендерингу цієї дії

### Список параметрів

`flag`

bool

> **Зауваження**
> 
> починаючи з 2.2.0, якщо цей параметр не заданий, буде повернено поточний стан

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafDispatcher::autoRender()****

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
     /* Метод init будет вызван, как только будет инициализирован контроллер */
     public function init() {
         if ($this->getRequest()->isXmlHttpRequest()) {
             //не вызывать render для ajax-запроса
             //мы выведем строку JSON
             Yaf_Dispatcher::getInstance()->autoRender(FALSE);
         }
     }

}
?>
```

Результатом виконання цього прикладу буде щось подібне:
