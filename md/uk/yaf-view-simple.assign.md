---
navigation:
  - class.yaf-view-simple.md: « Yaf\_View\_Simple
  - yaf-view-simple.assignref.md: 'Yaf\_View\_Simple::assignRef »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: Yaf\_View\_Simple
title: 'Yaf\_View\_Simple::assign'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_View\_Simple::assign

(Yaf >=1.0.0)

Yaf\_View\_Simple::assign — Призначити значення

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

**Пример #1 Пример использования**Yaf\_View\_Simple::assign()\*\*\*\*

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->assign("foo", "bar");
        $this->_view->assign( array( "key" => "value", "name" => "value"));
    }
}
?>
```

**Пример #2 Пример использования**template()\*\*\*\*

```php
<html>
 <head>
  <title><?php echo $foo; ?></title>
 </head>
<body>
  <?php

  foreach ($this->_tpl_vars as $name => $value) {
    echo $$name; // или echo $this->_tpl_vars[$name];
  }
  ?>
</body>
</html>
```

### Дивіться також

-   [Yaf\_View\_Simple::assignRef()](yaf-view-simple.assignref.md) \- Призначення assignRef
-   **Yaf\_View\_Interface::clear()**
-   [Yaf\_View\_Simple::\_\_set()](yaf-view-simple.set.md) \- Встановлює значення для двигуна
