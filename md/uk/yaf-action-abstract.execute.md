---
navigation:
  - class.yaf-action-abstract.md: « Yaf\_Action\_Abstract
  - yaf-action-abstract.getcontroller.md: 'Yaf\_Action\_Abstract::getController »'
  - index.md: PHP Manual
  - class.yaf-action-abstract.md: Yaf\_Action\_Abstract
title: 'Yaf\_Action\_Abstract::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Action\_Abstract::execute

(Yaf >=1.0.0)

Yaf\_Action\_Abstract::execute — Точка входу для Action-класів

### Опис

```methodsynopsis
abstract publicYaf_Action_Abstract::execute(mixed ...$args): mixed
```

Користувач повинен визначати цей метод для Action-класів, він є точкою входу до Action . **Yaf\_Action\_Abstract::execute()** може приймати аргументи.

> **Зауваження** :
> 
> Значення, яке отримується із запиту, не є безпечним. Ви повинні самостійно перевіряти його перед використанням.

### Список параметрів

`args`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Action\_Abstract::execute()\*\*\*\*

```php
<?php
/**
 * Пример контроллера
 */
class ProductController extends Yaf_Controller_Abstract {
      protected $actions = array(
          "index" => "actions/Index.php",
      );
}
?>
```

**Пример #2 Пример использования**Yaf\_Action\_Abstract::execute()\*\*\*\*

```php
<?php
/**
 * ListAction
 */
class ListAction extends Yaf_Action_Abstract {
     public function execute ($name, $id) {
         assert($name == $this->getRequest()->getParam("name"));
         assert($id   == $this->getRequest()->getParam("id"));
     }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
/**
 * Now assuming we are using the Yaf_Route_Static route
 * for request: http://yourdomain/product/list/name/yaf/id/22
 * will result:
 */
 bool(true)
 bool(true)
```

### Дивіться також
