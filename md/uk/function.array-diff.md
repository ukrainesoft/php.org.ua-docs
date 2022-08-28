Обчислити розбіжність масивів

-   [« array\_diff\_ukey](function.array-diff-ukey.html)
    
-   [array\_fill\_keys »](function.array-fill-keys.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с массивами](ref.array.html)
    
-   Обчислити розбіжність масивів
    

# arraydiff

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

arraydiff - Обчислити розбіжність масивів

### Опис

```methodsynopsis
array_diff(array $array, array ...$arrays): array
```

Порівнює `array` з одним або декількома іншими масивами і повертає значення з `array`, які відсутні у всіх інших масивах

### Список параметрів

`array`

Вихідний масив

`arrays`

Масиви, з якими йде порівняння

### Значення, що повертаються

Повертає масив (array), що містить елементи `array`відсутні в будь-якому з усіх інших масивів. Ключі в масиві `array` зберігаються.

### список змін

| Версия | Описание                                                                                             |
|--------|------------------------------------------------------------------------------------------------------|
|        | Функція тепер може бути викликана лише з одним параметром. Раніше потрібно не менше двох параметрів. |

### Приклади

**Приклад #1 Приклад використання **arraydiff()****

```php
<?php
$array1 = array("a" => "green", "red", "blue", "red");
$array2 = array("b" => "green", "yellow", "red");
$result = array_diff($array1, $array2);

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

**Приклад #2 Приклад використання **arraydiff()** з несхожими типами**

Два елементи вважаються рівними тоді і лише тоді, коли `(string) $elem1 === (string) $elem2`. Тобто коли [строковое представление](language.types.string.html#language.types.string.casting) однаково.

```php
<?php
// Это сгенерирует уведомление о том, что массив не может быть преобразован в строку.
$source = [1, 2, 3, 4];
$filter = [3, 4, [5], 6];
$result = array_diff($source, $filter);

// В то же время это нормально, поскольку объекты могут быть преобразованы в строку.
class S {
  private $v;

  public function __construct(string $v) {
    $this->v = $v;
  }

  public function __toString() {
    return $this->v;
  }
}

$source = [new S('a'), new S('b'), new S('c')];
$filter = [new S('b'), new S('c'), new S('d')];

$result = array_diff($source, $filter);

// $result теперь содержит один экземпляр S('a');
?>
```

Щоб використати альтернативну функцію порівняння, дивіться [array\_udiff()](function.array-udiff.html)

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що ця функція обробляє лише один вимір n-розмірного масиву. Звичайно, ви можете обробляти і більш глибокі рівні вкладеності, наприклад, використовуючи `array_diff($array1[0], $array2[0]);`

### Дивіться також

-   [array\_diff\_assoc()](function.array-diff-assoc.html) - обчислює розбіжність масивів з додатковою перевіркою індексу
-   [array\_udiff()](function.array-udiff.html) - обчислює розбіжність масивів, використовуючи для порівняння callback-функцію
-   [array\_intersect()](function.array-intersect.html) - обчислює сходження масивів
-   [array\_intersect\_assoc()](function.array-intersect-assoc.html) - обчислює сходження масивів з додатковою перевіркою індексу