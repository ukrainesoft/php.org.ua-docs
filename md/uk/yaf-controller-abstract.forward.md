---
navigation:
  - yaf-controller-abstract.display.md: '« Yaf\_Controller\_Abstract::display'
  - yaf-controller-abstract.getinvokearg.md: 'Yaf\_Controller\_Abstract::getInvokeArg »'
  - index.md: PHP Manual
  - class.yaf-controller-abstract.md: Yaf\_Controller\_Abstract
title: 'Yaf\_Controller\_Abstract::forward'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Controller\_Abstract::forward

(Yaf >=1.0.0)

Yaf\_Controller\_Abstract::forward — Переходить до іншої дії

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

> **Зауваження** :
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Yaf\_Controller\_Abstract::forward()\*\*\*\*

```php
<?php
class IndexController extends Yaf_Controller_Abstract
{
    public function indexAction(){
         $logined = $_SESSION["login"];
         if (!$logined) {
             $this->forward("login", array("from" => "Index")); // вперёд к действию login
             return FALSE;  // это важно, это закончить текущий рабочий поток
                            // и сказать Yaf не делать авторендеринг
         }

         // other processes
    }

    public function loginAction() {
         echo "Вход, перенаправлено с действия ", $this->_request->getParam("from");
    }
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Вход, перенаправлено с действия Index
```

### Дивіться також

-   **Yaf\_Request\_Abstrace::getParam()**
