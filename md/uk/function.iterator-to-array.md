Копіює ітератор у масив

-   [« iteratorcount](function.iterator-count.html)
    
-   [splautoloadcall »](function.spl-autoload-call.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SPL](ref.spl.html)
    
-   Копіює ітератор у масив
    

# iteratorтоarray

(PHP 5> = 5.1.0, PHP 7, PHP 8)

iteratorтоarray - Копіює ітератор в масив

### Опис

```methodsynopsis
iterator_to_array(Traversable $iterator, bool $preserve_keys = true): array
```

Копіює елементи ітератора масив.

### Список параметрів

`iterator`

Копіюваний ітератор.

`preserve_keys`

Чи слід використовувати ключі елементів ітератора як індекси?

Якщо ключ є масивом (array) чи об'єктом (object), кидається попередження. Ключі зі значенням **`null`** перетворюються на порожній рядок, ключі у вигляді чисел з плаваючою точкою (float) обрізаються до їх цілих (int) частин, ключі з ресурсами (resource) кидають попередження і перетворюються на їх ідентифікатори ресурсу, а логічні (bool) ключі перетворюються на цілі числа.

> **Зауваження**
> 
> Якщо параметр не заданий, або заданий як **`true`**, дублюючі ключі будуть перезаписані. Останнє значення із заданим ключем буде в результуючому масиві. Встановіть цей параметр рівним **`false`** для здобуття всіх значень.

### Значення, що повертаються

Масив, що містить елементи `iterator`

### Приклади

**Приклад #1 Приклад використання **iteratorтоarray()****

```php
<?php
$iterator = new ArrayIterator(array('recipe'=>'pancakes', 'egg', 'milk', 'flour'));
var_dump(iterator_to_array($iterator, true));
var_dump(iterator_to_array($iterator, false));
?>
```

Результат виконання цього прикладу:

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