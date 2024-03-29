---
navigation:
  - function.asort.md: « asort
  - function.count.md: count »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: compact
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# compact

(PHP 4, PHP 5, PHP 7, PHP 8)

compact — Створює масив, що містить назви змінних та їх значення

### Опис

```methodsynopsis
compact(array|string $var_name, array|string ...$var_names): array
```

Створює масив, що містить змінні та їх значення.

Для каждого переданного аргумента функция**compact()** шукає в поточній таблиці символів змінну з таким же ім'ям і додає її в масив, що виводиться так, що ім'я змінної стає ключем, а значення змінної стає значенням цього ключа. Коротше, вона виконує операцію, протилежну до функції [extract()](function.extract.md)

> **Зауваження** :
> 
> До PHP 7.3 рядки, для яких не знайшли змінні, будуть пропущені без генерації помилки.

### Список параметрів

`var_name`

`var_names`

Функция**compact()** приймає необмежену кількість аргументів. Будь-який з аргументів може бути рядком, що містить назву змінної, або масивом назв змінних. Масив може містити вкладені масиви назв змінних; функція **compact()** обробляє їх рекурсивно.

### Значення, що повертаються

Повертає масив із доданими змінними.

### Помилки

Функция**compact()** видає помилку рівня \*\*`E_WARNING`\*\*якщо отриманий рядок посилається на невизначену змінну.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо заданий рядок посилається на невизначену змінну, тепер буде згенеровано помилку рівня **`E_WARNING`** |
| 7.3.0 | Функция**compact()** тепер видає помилку рівня \*\*`E_NOTICE`\*\*якщо заданий рядок пов'язаний з невизначеною змінною. Раніше такі рядки пропускалися без попередження. |

### Приклади

**Приклад #1 Приклад використання** compact()\*\*\*\*

```php
<?php
$city  = "San Francisco";
$state = "CA";
$event = "SIGGRAPH";

$location_vars = array("city", "state");

$result = compact("event", $location_vars);
print_r($result);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [event] => SIGGRAPH
    [city] => San Francisco
    [state] => CA
)
```

### Примітки

> **Зауваження** **Зауваження щодо роботи функції compact**
> 
> Так как[змінні змінних](language.variables.variable.md) не можуть бути використані з [суперглобальними масивами](language.variables.superglobals.md) всередині функцій, суперглобальні масиви не можуть бути передані в **compact()**

### Дивіться також

-   [extract()](function.extract.md) \- Імпортує змінні масиву до поточної таблиці символів
