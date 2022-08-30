Переходить до іншої дії

-   [« YafControllerAbstract::display](yaf-controller-abstract.display.html)
    
-   [YafControllerAbstract::getInvokeArg »](yaf-controller-abstract.getinvokearg.html)
    
-   [PHP Manual](index.html)
    
-   [YafControllerAbstract](class.yaf-controller-abstract.html)
    
-   Переходить до іншої дії
    

# YafControllerAbstract::forward

(Yaf >=1.0.0)

YafControllerAbstract::forward — Переходить до іншої дії

### Опис

```methodsynopsis
public Yaf_Controller_Abstract::forward(string $action, array $paramters = ?): bool
```

```methodsynopsis
public Yaf_Controller_Abstract::forward(string $controller, string $action, array $paramters = ?): bool
```

```methodsynopsis
public Yaf_Controller_Abstract::forward(    string $module,    string $controller,    string $action,    array $paramters = ?): bool
```

Перенаправляє поточний процес виконання на іншу дію.

> **Зауваження**
> 
> Метод не перемикається на вказану дію негайно, перехід відбувається після завершення поточного потоку.

### Список параметрів

`module`

Ім'я цільового модуля, якщо встановлено NULL, то мається на увазі ім'я модуля за умовчанням

`controller`

Ім'я цільового контролера

`action`

Ім'я цільової дії

`paramters`

Аргументи виклику

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **YafControllerAbstract::forward()****

```php
<?php
class IndexController extends Yaf_Controller_Abstract
{
    public function indexAction(){
         $logined = $_SESSION["login"];
         if (!$logined) {
             $this->forward("login", array("from" => "Index")); // вперёд к действию login
             return FALSE;  // это важно, это закончить текущий рабочий поток
                            // и сказать Yaf не делать авторендеринг
         }

         // other processes
    }

    public function loginAction() {
         echo "Вход, перенаправлено с действия ", $this->_request->getParam("from");
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Вход, перенаправлено с действия Index
```

### Дивіться також

-   **YafRequestAbstrace::getParam()**