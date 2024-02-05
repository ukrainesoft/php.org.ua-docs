---
navigation:
  - function.array-diff-ukey.md: « array\_diff\_ukey
  - function.array-fill-keys.md: array\_fill\_keys »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_diff
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_diff

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

array\_diff - Обчислює розбіжність масивів

### Опис

```methodsynopsis
array_diff(array $array, array ...$arrays): array
```

Порівнює масив, переданий у параметр `array`, з одним або декількома іншими масивами та повертає значення з масиву `array`, які відсутні у всіх інших масивах

### Список параметрів

`array`

Вихідний масив

`arrays`

Масиви, з якими йде порівняння

### Значення, що повертаються

Повертає масив (array), що містить ті елементи масиву `array`, яких немає у будь-якому іншому масиві. Ключі в масиві `array` зберігаються.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер функцію можна викликати лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання** array\_diff()\*\*\*\*

```php
<?php
$array1 = array("a" => "green", "red", "blue", "red");
$array2 = array("b" => "green", "yellow", "red");
$result = array_diff($array1, $array2);

print_r($result);
?>
```

Множинні збіги $array1 обробляються як одне. Результат буде наступним:

```
Array
(
    [1] => blue
)
```

**Приклад #2 Приклад використання** array\_diff()\*\* з несхожими типами\*\*

Два елементи вважаються рівними тоді і лише тоді, коли `(string) $elem1 === (string) $elem2`. Тобто коли [рядкове подання](language.types.string.md#language.types.string.casting)одинаково.

```php
<?php
// Это сгенерирует уведомление о том, что массив не может быть преобразован в строку.
$source = [1, 2, 3, 4];
$filter = [3, 4, [5], 6];
$result = array_diff($source, $filter);

// В то же время это нормально, поскольку объекты могут быть преобразованы в строку.
class S {
  private $v;

  public function __construct(string $v) {
    $this->v = $v;
  }

  public function __toString() {
    return $this->v;
  }
}

$source = [new S('a'), new S('b'), new S('c')];
$filter = [new S('b'), new S('c'), new S('d')];

$result = array_diff($source, $filter);

// $result теперь содержит один экземпляр S('a');
?>
```

Щоб використати альтернативну функцію порівняння, дивіться [array\_udiff()](function.array-udiff.md)

### Примітки

> **Зауваження** :
> 
> Зверніть увагу, що ця функція обробляє лише один вимір n-розмірного масиву. Звичайно, ви можете обробляти і більш глибокі рівні вкладеності, наприклад, використовуючи `array_diff($array1[0], $array2[0]);`

### Дивіться також

-   [array\_diff\_assoc()](function.array-diff-assoc.md) \- обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_udiff()](function.array-udiff.md) \- обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_intersect()](function.array-intersect.md) \- обчислює перетин масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.md) \- обчислює перетин масивів з додатковою перевіркою індексу
