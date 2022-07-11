- [«array_intersect_ukey](function.array-intersect-ukey.md)
- [array_is_list »](function.array-is-list.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- обчислює сходження масивів

#array_intersect

(PHP 4 \>= 4.0.1, PHP 5, PHP 7, PHP 8)

array_intersect — обчислює сходження масивів

### Опис

**array_intersect**(array `$array`, array `...$arrays`): array

Функція **array_intersect()** повертає масив, що містить усі значення
масиву `array`, що містяться у всіх аргументах. Зверніть
увагу, що ключі зберігаються.

### Список параметрів

`array`
Основний масив, що перевіряється

`arrays`
Масиви, з якими йде порівняння значень

### Значення, що повертаються

Повертає масив, що містить усі значення `array`, які існують
у всіх переданих аргументах.

### Приклади

**Приклад #1 Приклад використання **array_intersect()****

` <?php$array1 = array("a" => "green", "red", "blue");$array2 = array("b" => "green", "yellow", "red"); $result = array_intersect($array1, $array2);print_r($result);?> `

Результат виконання цього прикладу:

Array
(
[a] => green
[0] => red
)

### Примітки

> **Примітка**: Два елементи вважаються однаковими тоді і лише
> тоді, коли `(string) $ elem1 === (string) $ elem2 `. Іншими словами,
> коли їх рядкові уявлення ідентичні.

### Дивіться також

- [array_intersect_assoc()](function.array-intersect-assoc.md) -
Обчислює сходження масивів із додатковою перевіркою індексу
- [array_diff()](function.array-diff.md) - Обчислити розбіжність
масивів
- [array_diff_assoc()](function.array-diff-assoc.md) - Обчислює
розбіжність масивів з додатковою перевіркою індексу
