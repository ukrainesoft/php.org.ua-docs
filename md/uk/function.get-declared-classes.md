---
navigation:
  - function.get-class.md: « get\_class
  - function.get-declared-interfaces.md: get\_declared\_interfaces »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_declared\_classes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_declared\_classes

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_declared\_classes — Повертає масив з іменами оголошених класів

### Опис

```methodsynopsis
get_declared_classes(): array
```

Повертає оголошені класи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив імен оголошених класів у поточному скрипті.

> **Зауваження** :
> 
> Врахуйте також, що в залежності від модулів, зібраних або завантажених у PHP, може змінюватись кількість додаткових класів. Це означає, що ви не можете використовувати власні класи з цими іменами. Список визначених класів перебуває у розділі доповнення "[Обумовлені класи](reserved.classes.md)".

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Раніше **get\_declared\_classes()** завжди повертала батьківські класи перед дочірніми класами. Це не так. Для значення, що повертається **get\_declared\_classes()** Конкретний порядок не гарантується. |

### Приклади

**Приклад #1 Приклад використання** get\_declared\_classes()\*\*\*\*

```php
<?php
print_r(get_declared_classes());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => stdClass
    [1] => __PHP_Incomplete_Class
    [2] => Directory
)
```

### Дивіться також

-   [class\_exists()](function.class-exists.md) \- Перевіряє, чи був оголошений клас
-   [get\_declared\_interfaces()](function.get-declared-interfaces.md) \- Повертає масив усіх оголошених інтерфейсів
-   [get\_defined\_functions()](function.get-defined-functions.md) \- Повертає масив усіх певних функцій
