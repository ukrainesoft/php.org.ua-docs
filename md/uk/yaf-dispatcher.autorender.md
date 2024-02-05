---
navigation:
  - class.yaf-dispatcher.md: « Yaf\_Dispatcher
  - yaf-dispatcher.catchexception.md: 'Yaf\_Dispatcher::catchException »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: Yaf\_Dispatcher
title: 'Yaf\_Dispatcher::autoRender'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Dispatcher::autoRender

(Yaf >=1.0.0)

Yaf\_Dispatcher::autoRender — Включає/вимикає авторендеринг

### Опис

```methodsynopsis
public Yaf_Dispatcher::autoRender(bool $flag = ?): Yaf_Dispatcher
```

[Yaf\_Dispatcher](class.yaf-dispatcher.md) буде відображатися автоматично після надсилання вхідного запиту. Ви можете запобігти рендерингу, викликавши цей метод за допомогою `flag` **`true`**

> **Зауваження** :
> 
> Ви можете просто повернути **`false`** у дії, щоб запобігти автоматичному рендерингу цієї дії

### Список параметрів

`flag`

bool

> **Зауваження** :
> 
> починаючи з 2.2.0, якщо цей параметр не заданий, буде повернено поточний стан

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Dispatcher::autoRender()\*\*\*\*

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
     /* Метод init будет вызван, как только будет инициализирован контроллер */
     public function init() {
         if ($this->getRequest()->isXmlHttpRequest()) {
             //не вызывать render для ajax-запроса
             //мы выведем строку JSON
             Yaf_Dispatcher::getInstance()->autoRender(FALSE);
         }
     }

}
?>
```

Висновок наведеного прикладу буде схожим на:
