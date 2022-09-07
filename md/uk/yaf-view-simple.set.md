---
navigation:
  - yaf-view-simple.render.md: '« YafViewSimple::render'
  - yaf-view-simple.setscriptpath.md: 'YafViewSimple::setScriptPath »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: YafViewSimple
title: 'YafViewSimple::set'
---
# YafViewSimple::set

(Yaf >=1.0.0)

YafViewSimple::set - Встановлює значення для движка

### Опис

```methodsynopsis
public Yaf_View_Simple::__set(string $name, mixed $value): void
```

Альтернативний і простий спосіб [YafViewSimple::assign()](yaf-view-simple.assign.md)

### Список параметрів

`name`

Ім'я строкового значення.

`value`

Різне значення.

### Значення, що повертаються

### Приклади

\*\*Приклад #1 Приклад використання \*\*YafViewSimple::set()**exampl**

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->foo = "bar"; // то же, что и assign("foo", "bar");
    }
}
?>
```

### Дивіться також

-   [YafViewSimple::assignRef()](yaf-view-simple.assignref.md) - Призначення assignRef
-   [YafViewInterface::assign()](yaf-view-interface.assign.md) - Призначає значення для движка відображення
