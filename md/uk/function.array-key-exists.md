---
navigation:
  - function.array-is-list.md: « array\_is\_list
  - function.array-key-first.md: array\_key\_first »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_key\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_key\_exists

(PHP 4 >= 4.0.7, PHP 5, PHP 7, PHP 8)

array\_key\_exists — Перевіряє, чи існує у масиві заданий ключ чи індекс

### Опис

```methodsynopsis
array_key_exists(string|int|float|bool|resource|null $key, array $array): bool
```

Функция**array\_key\_exists()** повертає **`true`**, якщо заданий ключ (`key`) міститься у масиві. У параметр `key` дозволено передавати значення, яке припустимо як індекс масиву.

### Список параметрів

`key`

Перевірене значення.

`array`

Масив з ключами, що перевіряються.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

> **Зауваження** :
> 
> Функция**array\_key\_exists()** шукає ключі лише на першому рівні масиву. Внутрішні ключі в багатовимірних масивах не знайдено.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`key` тепер приймає як аргументи значення `bool` `float` `int` `null` `resource`и`string` |

### Приклади

**Приклад #1 Приклад использования функции**array\_key\_exists()\*\*\*\*

```php
<?php

$search_array = array('first' => 1, 'second' => 4);
if (array_key_exists('first', $search_array)) {
    echo "Массив содержит элемент «first».";
}

?>
```

**Приклад #2 Приклад использования функции**array\_key\_exists()\*\* з мовною конструкцією [isset()](function.isset.md)\*\*

Конструкція мови [isset()](function.isset.md) не повертає **`true`** для ключів масиву, які асоційовані зі значенням **`null`**, а функция**array\_key\_exists()** - Повертає.

```php
<?php

$search_array = array('first' => null, 'second' => 4);

// Возвращает false
isset($search_array['first']);

// Возвращает true
array_key_exists('first', $search_array);

?>
```

### Примітки

> **Зауваження** :
> 
> З причин зворотної сумісності функція **array\_key\_exists()** повертає **`true`**, якщо ключ (`key`) — це властивість об'єкта (object), переданого як параметр `array`. Поведінка застаріла в PHP 7.4.0 та видалена в PHP 8.0.0.
> 
> Перевірити, чи містить об'єкт задану властивість, можна функцією [property\_exists()](function.property-exists.md)

### Дивіться також

-   [isset()](function.isset.md) \- Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [array\_keys()](function.array-keys.md) \- Повертає все або деяке підмножина ключів масиву
-   [in\_array()](function.in-array.md) \- Перевіряє, чи є у масиві значення
-   [property\_exists()](function.property-exists.md) \- Перевіряє, чи містить об'єкт чи клас атрибут
