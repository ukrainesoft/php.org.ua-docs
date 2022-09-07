---
navigation:
  - yaf-view-simple.assignref.md: '« YafViewSimple::assignRef'
  - yaf-view-simple.construct.md: 'YafViewSimple::construct »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: YafViewSimple
title: 'YafViewSimple::clear'
---
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
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->clear("foo")->clear("bar"); // очистить "foo" и "bar"
        $this->_view->clear(); //очистить все назначенные переменные
    }
}
?>
```

### Дивіться також

-   [YafViewSimple::assignRef()](yaf-view-simple.assignref.md) - Призначення assignRef
-   [YafViewInterface::assign()](yaf-view-interface.assign.md) - Призначає значення для движка відображення
-   [YafViewSimple::set()](yaf-view-simple.set.md) - Встановлює значення для двигуна
