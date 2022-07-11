- [«str_shuffle](function.str-shuffle.md)
- [str_starts_with »](function.str-starts-with.md)

- [PHP Manual](index.md)
- [Функції для роботи з рядками](ref.strings.md)
- Перетворює рядок на масив

#str_split

(PHP 5, PHP 7, PHP 8)

str_split — Перетворює рядок на масив

### Опис

**str_split**(string `$string`, int `$length` = 1): array

Перетворює рядок на масив.

### Список параметрів

`string`
Вхідний рядок.

`length`
Максимальна довжина фрагмента.

### Значення, що повертаються

Якщо вказано необов'язковий аргумент `length`, масив, що повертається
містити частини вихідного рядка довжиною `length` кожна, інакше кожен
елемент міститиме один символ.

Якщо `length` менше 1, повертається **`false`**. Якщо `length` більше
довжини рядка `string`, то весь рядок буде повернутий у першому та
єдиний елемент масиву.

### Приклади

**Приклад #1 Приклад використання **str_split()****

` <?php$str = "Hello Friend";$arr1 = str_split($str);$arr2 = str_split($str, 3);print_r($arr1);print_r($arr2);?> `

Результат виконання цього прикладу:

Array
(
[0] => H
[1] => e
[2] => l
[3] => l
[4] => o
[5] =>
[6] => F
[7] => r
[8] => i
[9] => e
[10] => n
[11] => d
)

Array
(
[0] => Hel
[1] => lo
[2] => Fri
[3] => end
)

### Примітки

> **Примітка**:
>
> Функція **str_split()** розбиває по байтах, а не по
> символів у разі використання рядків у багатобайтних кодуваннях.
> Використовуйте [mb_str_split()](function.mb-str-split.md),
> щоб розбити рядок на кодові точки.

### Дивіться також

- [mb_str_split()](function.mb-str-split.md) - Якщо задана
багатобайтовий рядок повертає масив символів
- [chunk_split()](function.chunk-split.md) - Розбиває рядок на
фрагменти
- [preg_split()](function.preg-split.md) - Розбиває рядок по
регулярному виразу
- [explode()](function.explode.md) - Розбиває рядок за допомогою
роздільника
- [count_chars()](function.count-chars.md) - Повертає інформацію про
символи, що входять до рядка
- [str_word_count()](function.str-word-count.md) - Повертає
інформацію про слова, що входять до рядка
- [for](control-structures.for.md)
