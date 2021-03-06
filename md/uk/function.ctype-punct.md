- [«ctype_print](function.ctype-print.md)
- [ctype_space »](function.ctype-space.md)

- [PHP Manual](index.md)
- [Функції Ctype](ref.ctype.md)
- Перевіряє наявність друкованих символів, які не містять пробільні
або буквено-цифрові символи

#ctype_punct

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

ctype_punct — Перевірка наявності друкованих символів, які не містять
пробільні або буквено-цифрові символи

### Опис

**ctype_punct**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$text`): bool

Перевіряє, чи всі символи в переданому рядку `text` є знаками
пунктуації.

### Список параметрів

`text`
Перевірений рядок.

> **Примітка**:
>
> Якщо передано ціле число (int) у діапазоні між -128 та 255
> включно, воно буде оброблено як ASCII-код одного символу (до
> негативним значенням буде додано 256 для можливості
> представлення символів із розширеного діапазону ASCII). Будь-яке інше
> ціле число буде оброблено як рядок, що містить десяткові цифри
> цього числа.

**Увага**
Починаючи з PHP 8.1.0, передача нерядкових аргументів застаріла. В майбутньому
аргумент буде інтерпретуватися як рядок замість коду ASCII. В
Залежно від передбачуваної поведінки аргумент повинен бути приведений до
рядку (string) або має бути зроблений явний виклик функції
[chr()](function.chr.md).

### Значення, що повертаються

Повертає **`true`**, якщо кожен символ у рядку `text` є
друкованим, але не є ні буквою, ні цифрою чи пробілом, та
**`false`** інакше. При виклику з порожнім рядком результатом
завжди буде **`false`**.

### Приклади

**Приклад #1 Приклад використання **ctype_punct()****

` <?php$strings = array('ABasdk!@!$#', '!@ # $', '*&$()');foreach ($strings as $testcase) {    if (ctype_punct($test ) {         echo "Рядок$testcase складається тільки із знаків пунктуації.
";    }}else {         echo "Рядок$testcase не складається тільки із знаків пунктуації.
";    }}?> `

Результат виконання цього прикладу:

Рядок ABasdk!@!$# не складається лише із знаків пунктуації.
Рядок !@ # $ не складається лише із знаків пунктуації.
Рядок *&$() складається лише із знаків пунктуації.

### Дивіться також

- [ctype_cntrl()](function.ctype-cntrl.md) - Перевіряє наявність
керуючих символів
- [ctype_graph()](function.ctype-graph.md) - Перевіряє наявність будь-яких
друкованих символів, крім пробілу
