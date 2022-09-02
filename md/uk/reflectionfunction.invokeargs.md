---
navigation:
  - reflectionfunction.invoke.md: '« ReflectionFunction::invoke'
  - reflectionfunction.isdisabled.md: 'ReflectionFunction::isDisabled »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::invokeArgs'
---
# ReflectionFunction::invokeArgs

(PHP 5> = 5.1.2, PHP 7, PHP 8)

ReflectionFunction::invokeArgs — Виклик функції передачі аргументів

### Опис

```methodsynopsis
public ReflectionFunction::invokeArgs(array $args): mixed
```

Викликає функцію та передає їй аргументи у вигляді масиву.

### Список параметрів

`args`

Передані функції аргументи як масиву. Поведінка функції аналогічна [calluserfuncarray()](function.call-user-func-array.md)

### Значення, що повертаються

Повертає результат виконання викликаної функції.

### Приклади

**Приклад #1 Приклад використання **ReflectionFunction::invokeArgs()****

```php
<?php
function title($title, $name)
{
    return sprintf("%s. %s\r\n", $title, $name);
}

$function = new ReflectionFunction('title');

echo $function->invokeArgs(array('Dr', 'Phil'));
?>
```

Результат виконання цього прикладу:

```
Dr. Phil
```

**Приклад #2 Приклад використання **ReflectionFunction::invokeArgs()** з посиланнями на аргументи**

```php
<?php
function get_false_conditions(array $conditions, array &$false_conditions)
{
    foreach ($conditions as $condition) {
        if (!$condition) {
            $false_conditions[] = $condition;
        }
    }
}

$function_ref     = new ReflectionFunction('get_false_conditions');

$conditions       = array(true, false, -1, 0, 1);
$false_conditions = array();

$function_ref->invokeArgs(array($conditions, &$false_conditions));

var_dump($false_conditions);
?>
```

Результат виконання цього прикладу:

```
array(2) {
  [0]=>
  bool(false)
  [1]=>
  int(0)
}
```

### Примітки

> **Зауваження**
> 
> Якщо функція має аргументи, які мають бути посиланнями, то вони мають бути посиланнями та в переданому спиці аргументів.

### Дивіться також

-   [ReflectionFunction::invoke()](reflectionfunction.invoke.md) - Викликає функцію
-   [ReflectionFunctionAbstract::getNumberOfParameters()](reflectionfunctionabstract.getnumberofparameters.md) - Отримує кількість параметрів
-   [invoke()](language.oop5.magic.md#object.invoke)
-   [calluserfuncarray()](function.call-user-func-array.md) - Викликає callback-функцію з масивом параметрів
