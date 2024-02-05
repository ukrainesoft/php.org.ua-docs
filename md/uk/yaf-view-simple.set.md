---
navigation:
  - yaf-view-simple.render.md: '« Yaf\_View\_Simple::render'
  - yaf-view-simple.setscriptpath.md: 'Yaf\_View\_Simple::setScriptPath »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: Yaf\_View\_Simple
title: 'Yaf\_View\_Simple::\_\_set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_View\_Simple::\_\_set

(Yaf >=1.0.0)

Yaf\_View\_Simple::\_\_set - Встановлює значення для движка

### Опис

```methodsynopsis
public Yaf_View_Simple::__set(string $name, mixed $value): void
```

Альтернативний і простий спосіб [Yaf\_View\_Simple::assign()](yaf-view-simple.assign.md)

### Список параметрів

`name`

Ім'я рядкового значення.

`value`

Різне значення.

### Значення, що повертаються

### Приклади

\*\*Приклад #1 Приклад використання \*\*Yaf\_View\_Simple::\_\_set()**exampl**

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

-   [Yaf\_View\_Simple::assignRef()](yaf-view-simple.assignref.md) \- Призначення assignRef
-   [Yaf\_View\_Interface::assign()](yaf-view-interface.assign.md) \- Призначає значення для движка відображення
