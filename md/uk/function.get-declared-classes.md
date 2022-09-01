---
navigation:
  - function.get-class.html: « getclass
  - function.get-declared-interfaces.html: getdeclaredinterfaces »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getdeclaredclasses
---
# getdeclaredclasses

(PHP 4, PHP 5, PHP 7, PHP 8)

getdeclaredclasses — Повертає масив з іменами оголошених класів

### Опис

```methodsynopsis
get_declared_classes(): array
```

Повертає оголошені класи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив імен оголошених класів у поточному скрипті.

> **Зауваження**
> 
> Врахуйте також, що в залежності від модулів, зібраних або завантажених у PHP, може змінюватись кількість додаткових класів. Це означає, що ви не можете використовувати власні класи з цими іменами. Список визначених класів перебуває у розділі доповнення "[Обумовлені класи](reserved.classes.md)".

### список змін

| Версия | Описание |
| --- | --- |
|  | Раніше **getdeclaredclasses()** завжди повертала батьківські класи перед дочірніми класами. Це не так. Для значення, що повертається **getdeclaredclasses()** Конкретний порядок не гарантується. |

### Приклади

**Приклад #1 Приклад використання **getdeclaredclasses()****

```php
<?php
print_r(get_declared_classes());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => stdClass
    [1] => __PHP_Incomplete_Class
    [2] => Directory
)
```

### Дивіться також

-   [classexists()](function.class-exists.md) - Перевіряє, чи був оголошений клас
-   [getdeclaredinterfaces()](function.get-declared-interfaces.md) - Повертає масив усіх оголошених інтерфейсів
-   [getdefinedfunctions()](function.get-defined-functions.md) - Повертає масив усіх певних функцій
