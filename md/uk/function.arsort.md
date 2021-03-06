- [«array](function.array.md)
- [asort »](function.asort.md)

- [PHP Manual](index.md)
- [Функції для роботи з масивами](ref.array.md)
- Сортує масив у порядку зменшення та підтримує асоціацію
індексів

# arsort

(PHP 4, PHP 5, PHP 7, PHP 8)

arsort — Сортує масив у порядку зменшення та підтримує асоціацію
індексів

### Опис

**arsort**(array `&$array`, int `$flags` = **`SORT_REGULAR`**): bool

Функція сортує `array` у порядку зменшення таким чином, що
зберігаються відносини між ключами та значеннями.

Вона корисна, в основному, при сортуванні асоціативних масивів, коли
важливо зберегти відношення ключ = значення.

> **Примітка**:
>
> Якщо обидва порівнювані значення еквівалентні, вони зберігають свій
> Початковий порядок. До PHP 8.0.0 їх відносний порядок
> відсортованому масиві був визначений.

> **Примітка**:
>
> Скидає внутрішній покажчик масиву перший елемент.

### Список параметрів

`array`
Вхідний масив.

`flags`
Необов'язковий другий параметр `flags` може використовуватись для
зміни поведінки сортування з використанням таких значень:

Прапори типу сортування:

- **`SORT_REGULAR`** - звичайне порівняння елементів; подробиці
описані в розділі [оператори порівняння](language.operators.comparison.md)
- **`SORT_NUMERIC`** - числове порівняння елементів
- **`SORT_STRING`** - рядкове порівняння елементів
- **`SORT_LOCALE_STRING`** - порівняння елементів як рядки на основі
поточний мовний стандарт. Використовується мовний стандарт,
який можна змінити за допомогою
[setlocale()](function.setlocale.md)
- **`SORT_NATURAL`** - порівняння елементів як рядки, використовуючи
"природний порядок", наприклад, [natsort()](function.natsort.md)
- **`SORT_FLAG_CASE`** - можна об'єднувати (побітове АБО) з
**`SORT_STRING`** або **`SORT_NATURAL`** для сортування рядків без
обліку регістру

### Значення, що повертаються

Функція завжди повертає **`true`**.

### Приклади

**Приклад #1 Приклад використання **arsort()****

` <?php$fruits = array("d" => "lemon", "a" => "orange", "b" => "banana", "c" => "apple");arsort($fruits );foreach ($fruits as $key => $val) {    echo "$key = $val
";}?> `

Результат виконання цього прикладу:

a = orange
d = lemon
b = banana
c = apple

Назви фруктів були відсортовані у зворотному порядку та ключі,
асоційовані з елементами, що були збережені.

### Дивіться також

- [sort()](function.sort.md) - Сортує масив за зростанням
- [asort()](function.asort.md) - Сортує масив у порядку
зростання та підтримує асоціацію індексів
- [Порівняння функцій сортування масивів](array.sorting.md)
