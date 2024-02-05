---
navigation:
  - function.array-reverse.md: « array\_reverse
  - function.array-shift.md: array\_shift »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_search
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_search

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

array\_search — Здійснює пошук даного значення в масиві та повертає ключ першого знайденого елемента у разі успішного виконання

### Опис

```methodsynopsis
array_search(mixed $needle, array $haystack, bool $strict = false): int|string|false
```

Шукає в `haystack`значение`needle`

### Список параметрів

`needle`

Шукане значення.

> **Зауваження** :
> 
> Якщо `needle` є рядком, порівняння відбувається з урахуванням регістру.

`haystack`

Масив.

`strict`

Если третий параметр`strict`установлен в\*\*`true`**, то функция**array\_search()\*\* шукатиме *ідентичні* елементи в `haystack`. Це означає, що також перевірятимуться [типи](language.types.md) `needle`в`haystack`, а об'єкти повинні бути одним і тим самим екземпляром.

### Значення, що повертаються

Повертає ключ для `needle`якщо він був знайдений у масиві, інакше **`false`**

Якщо `needle` присутній у `haystack` більше одного разу буде повернено перший знайдений ключ. Для повернення ключів для всіх знайдених значень використовуйте функцію [array\_keys()](function.array-keys.md) з необов'язковим параметром `search_value`

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Пример #1 Пример использования**array\_search()\*\*\*\*

```php
<?php
$array = array(0 => 'blue', 1 => 'red', 2 => 'green', 3 => 'red');

$key = array_search('green', $array); // $key = 2;
$key = array_search('red', $array);   // $key = 1;
?>
```

### Дивіться також

-   [array\_keys()](function.array-keys.md) \- Повертає все або деяке підмножина ключів масиву
-   [array\_values()](function.array-values.md) \- Повертає всі значення масиву
-   [array\_key\_exists()](function.array-key-exists.md) \- Перевіряє, чи існує в масиві заданий ключ чи індекс
-   [in\_array()](function.in-array.md) \- Перевіряє, чи є у масиві значення
