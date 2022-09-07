---
navigation:
  - function.array-reverse.md: « arrayreverse
  - function.array-shift.md: arrayshift »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arraysearch
---
# arraysearch

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

arraysearch — Здійснює пошук даного значення в масиві та повертає ключ першого знайденого елемента у разі успішного виконання

### Опис

```methodsynopsis
array_search(mixed $needle, array $haystack, bool $strict = false): int|string|false
```

Шукає в `haystack` значення `needle`

### Список параметрів

`needle`

Шукане значення.

> **Зауваження**
> 
> Якщо `needle` є рядком, порівняння відбувається з урахуванням регістру.

`haystack`

Масив.

`strict`

Якщо третій параметр `strict` встановлений в **`true`**, то функція **arraysearch()** шукатиме *ідентичні* елементи в `haystack`. Це означає, що також перевірятимуться [типи](language.types.md) `needle` в `haystack`, а об'єкти повинні бути одним і тим самим екземпляром.

### Значення, що повертаються

Повертає ключ для `needle`якщо він був знайдений у масиві, інакше **`false`**

Якщо `needle` присутній у `haystack` більше одного разу буде повернено перший знайдений ключ. Для повернення ключів для всіх знайдених значень використовуйте функцію [arraykeys()](function.array-keys.md) з необов'язковим параметром `search_value`

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.md). Використовуйте [оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання **arraysearch()****

```php
<?php
$array = array(0 => 'blue', 1 => 'red', 2 => 'green', 3 => 'red');

$key = array_search('green', $array); // $key = 2;
$key = array_search('red', $array);   // $key = 1;
?>
```

### Дивіться також

-   [arraykeys()](function.array-keys.md) - Повертає все або деяке підмножина ключів масиву
-   [arrayvalues()](function.array-values.md) - Вибирає всі значення масиву
-   [arraykeyexists()](function.array-key-exists.md) - Перевіряє, чи присутній у масиві зазначений ключ чи індекс
-   [інarray()](function.in-array.md) - Перевіряє, чи є у масиві значення
