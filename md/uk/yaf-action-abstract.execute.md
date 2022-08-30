Точка входу для Action-класів

-   [« YafActionAbstract](class.yaf-action-abstract.html)
    
-   [YafActionAbstract::getController »](yaf-action-abstract.getcontroller.html)
    
-   [PHP Manual](index.md)
    
-   [YafActionAbstract](class.yaf-action-abstract.html)
    
-   Точка входу для Action-класів
    

# YafActionAbstract::execute

(Yaf >=1.0.0)

YafActionAbstract::execute — Точка входу для Action-класів

### Опис

```methodsynopsis
abstract publicYaf_Action_Abstract::execute(mixed ...$args): mixed
```

Користувач повинен визначати цей метод для Action-класів, він є точкою входу до Action . **YafActionAbstract::execute()** може приймати аргументи.

> **Зауваження**
> 
> Значення, яке отримується із запиту, не є безпечним. Ви повинні самостійно перевіряти його перед використанням.

### Список параметрів

`args`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafActionAbstract::execute()****

```php
<?php
/**
 * Пример контроллера
 */
class ProductController extends Yaf_Controller_Abstract {
      protected $actions = array(
          "index" => "actions/Index.php",
      );
}
?>
```

**Приклад #2 Приклад використання **YafActionAbstract::execute()****

```php
<?php
/**
 * ListAction
 */
class ListAction extends Yaf_Action_Abstract {
     public function execute ($name, $id) {
         assert($name == $this->getRequest()->getParam("name"));
         assert($id   == $this->getRequest()->getParam("id"));
     }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

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