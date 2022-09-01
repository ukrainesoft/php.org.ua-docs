---
navigation:
  - yaf-view-simple.assign.html: '« YafViewSimple::assign'
  - yaf-view-simple.clear.html: 'YafViewSimple::clear »'
  - index.md: PHP Manual
  - class.yaf-view-simple.html: YafViewSimple
title: 'YafViewSimple::assignRef'
---
# YafViewSimple::assignRef

(Yaf >=1.0.0)

YafViewSimple::assignRef — Призначення assignRef

### Опис

```methodsynopsis
public Yaf_View_Simple::assignRef(string $name, mixed &$value): bool
```

На відміну від [YafViewSimple::assign()](yaf-view-simple.assign.md), цей метод надає значення ref движку.

### Список параметрів

`name`

Строкове ім'я, яке використовуватиметься для доступу до значення у шаблоні.

`value`

Різне значення

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafViewSimple::assignRef()****

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $value = "bar";
        $this->getView()->assign("foo", $value);

        /* обратите внимание, что до Yaf 2.1.4 была ошибка,
         * которая делает следующий вывод "bar";
         */
        $dummy = $this->getView()->render("index/index.phtml");
        echo $value;

        // предотвратить авто-рендеринг
        Yaf_Dispatcher::getInstance()->autoRender(FALSE);
    }
}
?>
```

**Приклад #2 Приклад використання **template()****

```php
<html>
 <head>
  <title><?php echo $foo;  $foo = "changed"; ?></title>
 </head>
<body>
</body>
</html>
```

Результатом виконання цього прикладу буде щось подібне:

```
/* доступ к IndexController: */
changed
```

### Дивіться також

-   [YafViewSimple::assign()](yaf-view-simple.assign.md) - Призначити значення
-   [YafViewSimple::set()](yaf-view-simple.set.md) - Встановлює значення для двигуна
