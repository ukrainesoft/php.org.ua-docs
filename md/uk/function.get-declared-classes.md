Повертає масив із іменами оголошених класів

-   [« get\_class](function.get-class.html)
    
-   [get\_declared\_interfaces »](function.get-declared-interfaces.html)
    
-   [PHP Manual](index.html)
    
-   [Функции работы с классами и объектами](ref.classobj.html)
    
-   Повертає масив із іменами оголошених класів
    

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
> Врахуйте також, що в залежності від модулів, зібраних або завантажених у PHP, може змінюватись кількість додаткових класів. Це означає, що ви не можете використовувати власні класи з цими іменами. Список визначених класів перебуває у розділі доповнення "[Предопределённые классы](reserved.classes.html)".

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

-   [class\_exists()](function.class-exists.html) - Перевіряє, чи був оголошений клас
-   [get\_declared\_interfaces()](function.get-declared-interfaces.html) - Повертає масив усіх оголошених інтерфейсів
-   [get\_defined\_functions()](function.get-defined-functions.html) - Повертає масив усіх певних функцій