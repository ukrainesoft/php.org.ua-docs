Скидає призначені значення

-   [« Yaf\_View\_Simple::assignRef](yaf-view-simple.assignref.html)
    
-   [Yaf\_View\_Simple::\_\_construct »](yaf-view-simple.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_View\_Simple](class.yaf-view-simple.html)
    
-   Скидає призначені значення
    

# YafViewSimple::clear

(Yaf> = 2.2.0)

YafViewSimple::clear — Скидає призначені значення

### Опис

```methodsynopsis
public Yaf_View_Simple::clear(string $name = ?): bool
```

Скидає призначені значення

### Список параметрів

`name`

Надане ім'я змінної

Якщо не вказано, очистить усі призначені змінні

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafViewSimple::clear()****

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->clear("foo")->clear("bar"); // очистить "foo" и "bar"
        $this->_view->clear(); //очистить все назначенные переменные
    }
}
?>
```

### Дивіться також

-   [Yaf\_View\_Simple::assignRef()](yaf-view-simple.assignref.html) - Призначення assignRef
-   [Yaf\_View\_Interface::assign()](yaf-view-interface.assign.html) - Призначає значення для движка відображення
-   [Yaf\_View\_Simple::\_\_set()](yaf-view-simple.set.html) - Встановлює значення для двигуна