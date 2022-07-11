- [«array_diff_ukey](function.array-diff-ukey.md)
- [array_fill_keys »](function.array-fill-keys.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Обчислити розбіжність масивів

#array_diff

(PHP 4 \>= 4.0.1, PHP 5, PHP 7, PHP 8)

array_diff - Обчислити розбіжність масивів

### Опис

**array_diff**(array `$array`, array `...$arrays`): array

Порівнює `array` з одним або декількома іншими масивами та
повертає значення з `array`, які відсутні у всіх інших
масивах.

### Список параметрів

`array`
Вихідний масив

`arrays`
Масиви, з якими йде порівняння

### Значення, що повертаються

Повертає масив (array), що містить елементи `array`, відсутні в
кожному з решти масивів. Ключі в масиві `array` зберігаються.

### Приклади

**Приклад #1 Приклад використання **array_diff()****

` <?php$array1 = array("a" => "green", "red", "blue", "red");$array2 = array("b" => "green", "yellow", " red");$result = array_diff($array1, $array2);print_r($result);?> `

Множинні збіги в $ array1 обробляються як одне. Результат
буде наступним:

Array
(
[1] => blue
)

**Приклад #2 Приклад використання **array_diff()** з несхожими
типами**

Два елементи вважаються рівними тоді і лише тоді, коли
`(string) $elem1 === (string) $elem2`. Тобто, коли [рядкове представлення](language.types.string.md#language.types.string.casting)
однаково.

` <?php// Це згенерує повідомлення про том, що масив не може перетворити в рядок.$source = [1, 2, 3, 4];$filter = [3, result = array_diff($source, $filter);// В то же час це нормально, оскільки об'єкти можуть бути перетворені в рядок.class S { private public function __construct(string$$) {   $this->v = $v; }  public function __toString() {    return $this->v; }}$source = [new S('a'), new S('b'), new S('c')];$filter = [new S('b'), new S('c') , new S('d')];$result = array_diff($source, $filter);// $result тепер містить один примірник S('a');?> `

Щоб використати альтернативну функцію порівняння, дивіться
[array_udiff()](function.array-udiff.md).

### Примітки

> **Примітка**:
>
> Зверніть увагу, що ця функція обробляє лише один вимір
> n-розмірного масиву. Звичайно, ви можете обробляти і більше
> глибокі рівні вкладеності, наприклад, використовуючи
> `array_diff($array1[0], $array2[0]);`.

### Дивіться також

- [array_diff_assoc()](function.array-diff-assoc.md) - Обчислює
розбіжність масивів з додатковою перевіркою індексу
- [array_udiff()](function.array-udiff.md) - Розраховує розбіжність
масивів, використовуючи для порівняння callback-функцію
- [array_intersect()](function.array-intersect.md) - Обчислює
сходження масивів
- [array_intersect_assoc()](function.array-intersect-assoc.md) -
Обчислює сходження масивів із додатковою перевіркою індексу
