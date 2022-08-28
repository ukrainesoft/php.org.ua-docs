Встановлює значення для двигуна

-   [« Yaf\_View\_Simple::render](yaf-view-simple.render.html)
    
-   [Yaf\_View\_Simple::setScriptPath »](yaf-view-simple.setscriptpath.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_View\_Simple](class.yaf-view-simple.html)
    
-   Встановлює значення для двигуна
    

# YafViewSimple::set

(Yaf >=1.0.0)

YafViewSimple::set - Встановлює значення для движка

### Опис

```methodsynopsis
public Yaf_View_Simple::__set(string $name, mixed $value): void
```

Альтернативний і простий спосіб [Yaf\_View\_Simple::assign()](yaf-view-simple.assign.html)

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
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $this->getView()->foo = "bar"; // то же, что и assign("foo", "bar");
    }
}
?>
```

### Дивіться також

-   [Yaf\_View\_Simple::assignRef()](yaf-view-simple.assignref.html) - Призначення assignRef
-   [Yaf\_View\_Interface::assign()](yaf-view-interface.assign.html) - Призначає значення для движка відображення