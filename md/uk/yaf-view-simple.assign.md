---
navigation:
  - class.yaf-view-simple.md: « YafViewSimple
  - yaf-view-simple.assignref.md: 'YafViewSimple::assignRef »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: YafViewSimple
title: 'YafViewSimple::assign'
---
# YafViewSimple::assign

(Yaf >=1.0.0)

YafViewSimple::assign — Призначити значення

### Опис

```methodsynopsis
public Yaf_View_Simple::assign(string $name, mixed $value = ?): bool
```

Призначає змінну для движка відображення

### Список параметрів

`name`

Рядок або масив.

Якщо це рядок, наступний аргумент $value є обов'язковим.

`value`

Різне значення

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafViewSimple::assign()****

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->assign("foo", "bar");
        $this->_view->assign( array( "key" => "value", "name" => "value"));
    }
}
?>
```

**Приклад #2 Приклад використання **template()****

```php
<html>
 <head>
  <title><?php echo $foo; ?></title>
 </head>
<body>
  <?php

  foreach ($this->_tpl_vars as $name => $value) {
    echo $$name; // или echo $this->_tpl_vars[$name];
  }
  ?>
</body>
</html>
```

### Дивіться також

-   [YafViewSimple::assignRef()](yaf-view-simple.assignref.md) - Призначення assignRef
-   **YafViewInterface::clear()**
-   [YafViewSimple::set()](yaf-view-simple.set.md) - Встановлює значення для двигуна
