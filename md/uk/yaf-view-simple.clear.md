---
navigation:
  - yaf-view-simple.assignref.md: '« Yaf\_View\_Simple::assignRef'
  - yaf-view-simple.construct.md: 'Yaf\_View\_Simple::\_\_construct »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: Yaf\_View\_Simple
title: 'Yaf\_View\_Simple::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_View\_Simple::clear

(Yaf >=2.2.0)

Yaf\_View\_Simple::clear — Скидає призначені значення

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

**Пример #1 Пример использования**Yaf\_View\_Simple::clear()\*\*\*\*

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

-   [Yaf\_View\_Simple::assignRef()](yaf-view-simple.assignref.md) \- Призначення assignRef
-   [Yaf\_View\_Interface::assign()](yaf-view-interface.assign.md) \- Призначає значення для движка відображення
-   [Yaf\_View\_Simple::\_\_set()](yaf-view-simple.set.md) \- Встановлює значення для двигуна
