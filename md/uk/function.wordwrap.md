---
navigation:
  - function.vsprintf.md: « vsprintf
  - changelog.strings.md: Список изменений »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: Wordwrap
---
# Wordwrap

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

wordwrap — Перенесення рядка за вказаною кількістю символів

### Опис

```methodsynopsis
wordwrap(    string $string,    int $width = 75,    string $break = "\n",    bool $cut_long_words = false): string
```

Переносить рядок за вказаною кількістю символів.

### Список параметрів

`string`

Вхідний рядок.

`width`

Кількість символів, за якими рядок буде перенесено.

`break`

Символ перенесення рядка можна вказати за допомогою необов'язкового параметра `break`

`cut_long_words`

Якщо параметр `cut_long_words` встановлений в **`true`**, рядок завжди буде переноситися на вказаній ширині `width` або раніше. Тому, якщо вихідний рядок містить слово довше заданої ширини рядка, воно буде розірвано. (Дивіться другий приклад). Якщо встановлений у **`false`**, функція не поділяє слово, навіть якщо `width` менше довжини слова.

### Значення, що повертаються

Повертає рядок із вставленими символами перенесення на вказаній довжині.

### Приклади

**Приклад #1 Приклад використання **wordwrap()****

```php
<?php
$text = "The quick brown fox jumped over the lazy dog.";
$newtext = wordwrap($text, 20, "<br />\n");

echo $newtext;
?>
```

Результат виконання цього прикладу:

```
The quick brown fox<br />
jumped over the lazy<br />
dog.
```

**Приклад #2 Приклад використання **wordwrap()****

```php
<?php
$text = "A very long woooooooooooord.";
$newtext = wordwrap($text, 8, "\n", true);

echo "$newtext\n";
?>
```

Результат виконання цього прикладу:

```
A very
long
wooooooo
ooooord.
```

**Приклад #3 Приклад використання **wordwrap()****

```php
<?php
$text = "A very long woooooooooooooooooord. and something";
$newtext = wordwrap($text, 8, "\n", false);

echo "$newtext\n";
?>
```

Результат виконання цього прикладу:

```
A very
long
woooooooooooooooooord.
and
something
```

### Дивіться також

-   [nl2br()](function.nl2br.md) - Вставляє HTML код розриву рядка перед кожним перекладом рядка
-   [chunksplit()](function.chunk-split.md) - Розбиває рядок на фрагменти
