---
navigation:
  - yaf-view-simple.assign.md: '« Yaf\_View\_Simple::assign'
  - yaf-view-simple.clear.md: 'Yaf\_View\_Simple::clear »'
  - index.md: PHP Manual
  - class.yaf-view-simple.md: Yaf\_View\_Simple
title: 'Yaf\_View\_Simple::assignRef'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_View\_Simple::assignRef

(Yaf >=1.0.0)

Yaf\_View\_Simple::assignRef — Призначення assignRef

### Опис

```methodsynopsis
public Yaf_View_Simple::assignRef(string $name, mixed &$value): bool
```

В отличие от[Yaf\_View\_Simple::assign()](yaf-view-simple.assign.md), цей метод надає значення ref движку.

### Список параметрів

`name`

Строкове ім'я, яке використовуватиметься для доступу до значення у шаблоні.

`value`

Різне значення

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_View\_Simple::assignRef()\*\*\*\*

```php
<?php
class IndexController extends Yaf_Controller_Abstract {
    public function indexAction() {
        $value = "bar";
        $this->getView()->assign("foo", $value);

        /* обратите внимание, что до Yaf 2.1.4 была ошибка,
         * которая делает следующий вывод "bar";
         */
        $dummy = $this->getView()->render("index/index.phtml");
        echo $value;

        // предотвратить авто-рендеринг
        Yaf_Dispatcher::getInstance()->autoRender(FALSE);
    }
}
?>
```

**Пример #2 Пример использования**template()\*\*\*\*

```php
<html>
 <head>
  <title><?php echo $foo;  $foo = "changed"; ?></title>
 </head>
<body>
</body>
</html>
```

Висновок наведеного прикладу буде схожим на:

```
/* доступ к IndexController: */
changed
```

### Дивіться також

-   [Yaf\_View\_Simple::assign()](yaf-view-simple.assign.md) \- Призначити значення
-   [Yaf\_View\_Simple::\_\_set()](yaf-view-simple.set.md) \- Встановлює значення для двигуна
