- [«array_reduce](function.array-reduce.md)
- [array_replace »](function.array-replace.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- рекурсивно замінює елементи першого масиву елементами переданих
масивів

#array_replace_recursive

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

array_replace_recursive — Рекурсивно замінює елементи першого масиву
елементами переданих масивів

### Опис

**array_replace_recursive**(array `$array`, array `...$replacements`):
array

**array_replace_recursive()** замінює значення масиву `array` на
відповідні за ключами значення всіх наступних масивів. Якщо ключ
з першого масиву є у другому, його значення буде замінено на
значення другого масиву. Якщо ключ є у другому масиві, але
відсутня у першому, він буде створений у першому масиві. Якщо ключ є
лише у першому масиві, він залишається як є. Якщо передано
кілька масивів, вони будуть оброблені по порядку, наступні
перезаписують попередні значення.

**array_replace_recursive()** - рекурсивна функція: вона буде
рекурсивно заглиблюватися в масиви та застосовувати до всіх внутрішніх значень
той самий процес.

Якщо значення, передане перший масив є скалярним, воно буде
замінено значенням у другому масиві, яке може бути скалярним
значенням чи масивом. Якщо обидва значення передані в перший масив і
у другий масив - масиви, **array_replace_recursive()** замінюватиме
їх значення рекурсивні.

### Список параметрів

`array`
Масив, елементи якого буде замінено.

`replacements`
Масиви, з яких братимуться елементи для заміни.

### Значення, що повертаються

Повертає масив (array) або **`null`**, якщо сталася помилка.

### Приклади

**Приклад #1 Приклад використання **array_replace_recursive()****

` <?php$base = array('citrus' => array( "orange") , 'berries' => array("blackberry", "raspberry"), );$replacements = array('citrus' =>> ('pineapple'), 'berries' => array('blueberry'));$basket = array_replace_recursive($base, $replacements);print_r($basket);$basket = array_replace($base, $replace ($ basket);?> `

Результат виконання цього прикладу:

Array
(
[citrus] => Array
(
[0] => pineapple
)

[berries] => Array
(
[0] => blueberry
[1] => raspberry
)

)
Array
(
[citrus] => Array
(
[0] => pineapple
)

[berries] => Array
(
[0] => blueberry
)

)

**Приклад #2 **array_replace_recursive()** та рекурсивна поведінка**

` <?php$base = array('citrus' => array("orange") , 'berries' => array("blackberry", "raspberry"), 'others' => 'banana' );$replacements array('citrus' => 'pineapple', 'berries' => array('blueberry'), 'others' => array('litchis'));$replacements2 = array('citrus' => array('e '), 'berries' => array('blueberry'), 'others' => 'litchis');$basket = array_replace_recursive($base, $replacements, $replacements2);print_r($basket);?>

Результат виконання цього прикладу:

Array
(
[citrus] => Array
(
[0] => pineapple
)

[berries] => Array
(
[0] => blueberry
[1] => raspberry
)

[others] => litchis
)

### Дивіться також

- [array_replace()](function.array-replace.md) - Замінює елементи
масиву елементами інших переданих масивів
- [array_merge_recursive()](function.array-merge-recursive.md) -
Рекурсивне злиття одного або більше масивів
