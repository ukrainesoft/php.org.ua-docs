---
navigation:
  - yaf-route-simple.assemble.md: '« Yaf\_Route\_Simple::assemble'
  - yaf-route-simple.route.md: 'Yaf\_Route\_Simple::route »'
  - index.md: PHP Manual
  - class.yaf-route-simple.md: Yaf\_Route\_Simple
title: 'Yaf\_Route\_Simple::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Simple::\_\_construct

(Yaf >=1.0.0)

Yaf\_Route\_Simple::\_\_construct - Конструктор класу Yaf\_Route\_Simple

### Опис

public **Yaf\_Route\_Simple::\_\_construct**(string`$module_name`, string`$controller_name`, string`$action_name`) .

[Yaf\_Route\_Simple](class.yaf-route-simple.md) отримає інформацію про маршрут з рядка запиту та параметри конструктора будуть використовуватись як ключі при пошуку інформації про маршрут у $\_GET.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`module_name`

Ім'я ключа інформації про модуль.

`controller_name`

Ім'я ключа інформації про контролера.

`action_name`

Ім'я ключа інформації про дію.

### Значення, що повертаються

Завжди повертає **`true`**

### Приклади

**Приклад #1 Приклад использования[Yaf\_Route\_Simple::route()](yaf-route-simple.route.md)**

```php
<?php
   $route = new Yaf_Route_Simple("m", "controller", "act");
   Yaf_Router::getInstance()->addRoute("simple", $route);
?>
```

**Приклад #2 Приклад использования[Yaf\_Route\_Simple::route()](yaf-route-simple.route.md)**

Запит: [http://yourdomain.com/path/?controller=a&act=b](http://yourdomain.com/path/?controller=a&act=b) => module = default(index), controller = a, action = b

Запит: [http://yourdomain.com/path](http://yourdomain.com/path) => module = default(index), controller = default(index), action = default(index)

### Дивіться також

-   [Yaf\_Route\_Supervar::route()](yaf-route-supervar.route.md) \- Призначення route
-   [Yaf\_Route\_Static::route()](yaf-route-static.route.md) \- Надсилає запит
-   [Yaf\_Route\_Regex::route()](yaf-route-regex.route.md) \- Мета маршруту
-   [Yaf\_Route\_Rewrite::route()](yaf-route-rewrite.route.md) \- Призначення route
-   [Yaf\_Route\_Map::route()](yaf-route-map.route.md) \- Призначення route
