Призначити значення

-   [« Yaf\_View\_Simple](class.yaf-view-simple.html)
    
-   [Yaf\_View\_Simple::assignRef »](yaf-view-simple.assignref.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_View\_Simple](class.yaf-view-simple.html)
    
-   Призначити значення
    

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

-   [Yaf\_View\_Simple::assignRef()](yaf-view-simple.assignref.html) - Призначення assignRef
-   **YafViewInterface::clear()**
-   [Yaf\_View\_Simple::\_\_set()](yaf-view-simple.set.html) - Встановлює значення для двигуна