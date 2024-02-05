---
navigation:
  - function.iterator-count.md: « iterator\_count
  - function.spl-autoload-call.md: spl\_autoload\_call »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: iterator\_to\_array
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# iterator\_to\_array

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

iterator\_to\_array - Копіює ітератор в масив

### Опис

```methodsynopsis
iterator_to_array(Traversable|array $iterator, bool $preserve_keys = true): array
```

Копіює елементи ітератора масив.

### Список параметрів

`iterator`

Копіюваний ітератор.

`preserve_keys`

Чи слід використовувати ключі елементів ітератора як індекси?

Якщо ключ є масивом (array) чи об'єктом (object), то кидається попередження. Ключі зі значенням **`null`** перетворюються на порожній рядок, ключі у вигляді чисел з плаваючою точкою (float) обрізаються до цілих (int) частин, ключі з ресурсами (resource) кидають попередження і перетворюються на їх ідентифікатори ресурсу, а логічні (bool) ключі перетворюються на цілі числа.

> **Зауваження** :
> 
> Если параметр не задан, либо задан как\*\*`true`\*\*, дублюючі ключі будуть перезаписані. Останнє значення із заданим ключем буде в результуючому масиві. Встановіть цей параметр рівним \*\*`false`\*\*для получения всех значений.

### Значення, що повертаються

Масив, що містить елементи `iterator`

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип параметра `iterator` був розширений з [Traversable](class.traversable.md)до[Traversable](class.traversable.md) |

### Приклади

**Приклад #1 Приклад використання** iterator\_to\_array()\*\*\*\*

```php
<?php
$iterator = new ArrayIterator(array('recipe'=>'pancakes', 'egg', 'milk', 'flour'));
var_dump(iterator_to_array($iterator, true));
var_dump(iterator_to_array($iterator, false));
?>
```

Результат виконання наведеного прикладу:

```
array(4) {
  ["recipe"]=>
  string(8) "pancakes"
  [0]=>
  string(3) "egg"
  [1]=>
  string(4) "milk"
  [2]=>
  string(5) "flour"
}
array(4) {
  [0]=>
  string(8) "pancakes"
  [1]=>
  string(3) "egg"
  [2]=>
  string(4) "milk"
  [3]=>
  string(5) "flour"
}
```
