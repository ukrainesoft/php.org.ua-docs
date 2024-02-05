---
navigation:
  - yaf-route-supervar.assemble.md: '« Yaf\_Route\_Supervar::assemble'
  - yaf-route-supervar.route.md: 'Yaf\_Route\_Supervar::route »'
  - index.md: PHP Manual
  - class.yaf-route-supervar.md: Yaf\_Route\_Supervar
title: 'Yaf\_Route\_Supervar::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Route\_Supervar::\_\_construct

(Yaf >=1.0.0)

Yaf\_Route\_Supervar::\_\_construct — Назначение\_\_construct

### Опис

public **Yaf\_Route\_Supervar::\_\_construct**(string`$supervar_name`) .

[Yaf\_Route\_Supervar](class.yaf-route-supervar.md)похож на[Yaf\_Route\_Static](class.yaf-route-static.md), Різниця в тому, що [Yaf\_Route\_Supervar](class.yaf-route-supervar.md) шукатиме інформацію про шлях у рядку запиту, а параметр supervar\_name є ключем.

### Список параметрів

`supervar_name`

Назва ключа.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** Yaf\_Route\_Supervar()\*\*\*\*

```php
<?php
   /**
    * Добавление маршрута supervar в стек маршрутов Yaf_Router
    */
    Yaf_Dispatcher::getInstance()->getRouter()->addRoute(
        "name",
        new Yaf_Route_Supervar("r")
    );
?>
```

Висновок наведеного прикладу буде схожим на:

```
/** для запроса: http://yourdomain.com/xx/oo/?r=/ctr/act/var/value
  * будет следующий результат:
  */
  array (
    "module"   => index(default),
    "controller" => ctr,
    "action"     => act,
    "params"     => array(
          "var" => value,
     )
  )
```

### Дивіться також

-   [Yaf\_Router::addRoute()](yaf-router.addroute.md) \- Додає новий маршрут до маршрутизатора
-   [Yaf\_Router::addConfig()](yaf-router.addconfig.md) \- Додає налаштовані маршрути до маршрутизатора
-   [Yaf\_Route\_Static](class.yaf-route-static.md)
-   [Yaf\_Route\_Regex](class.yaf-route-regex.md)
-   [Yaf\_Route\_Simple](class.yaf-route-simple.md)
-   [Yaf\_Route\_Rewrite](class.yaf-route-rewrite.md)
-   [Yaf\_Route\_Map](class.yaf-route-map.md)
