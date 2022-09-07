---
navigation:
  - function.extract.md: « extract
  - function.key-exists.md: keyexists »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: інarray
---
# інarray

(PHP 4, PHP 5, PHP 7, PHP 8)

інarray — Перевіряє, чи є у масиві значення

### Опис

```methodsynopsis
in_array(mixed $needle, array $haystack, bool $strict = false): bool
```

Шукає в `haystack` значення `needle`. Якщо `strict` не встановлений, то при пошуку буде використано не суворе порівняння.

### Список параметрів

`needle`

Шукане значення.

> **Зауваження**
> 
> Якщо `needle` - Рядок, порівняння буде зроблено з урахуванням регістру.

`haystack`

Масив.

`strict`

Якщо третій параметр `strict` встановлений в \*\*`true`\*\*тоді функція **інarray()** також перевірить відповідність [типов](language.types.md) параметра `needle` та відповідного значення масиву `haystack`

### Значення, що повертаються

Повертає **`true`**, якщо `needle` був знайдений у масиві, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **інarray()****

```php
<?php
$os = array("Mac", "NT", "Irix", "Linux");
if (in_array("Irix", $os)) {
    echo "Нашёл Irix";
}
if (in_array("mac", $os)) {
    echo "Нашёл mac";
}
?>
```

Другого збігу не буде, бо **інarray()** реєстрозалежна, таким чином, програма виведе:

```
Нашёл Irix
```

**Приклад #2 Приклад використання **інarray()** з параметром strict**

```php
<?php
$a = array('1.10', 12.4, 1.13);

if (in_array('12.4', $a, true)) {
    echo "'12.4' найдено со строгой проверкой\n";
}

if (in_array(1.13, $a, true)) {
    echo "1.13 найдено со строгой проверкой\n";
}
?>
```

Результат виконання цього прикладу:

```
1.13 найдено со строгой проверкой
```

**Приклад #3 Приклад використання **інarray()** з масивом як параметр needle**

```php
<?php
$a = array(array('p', 'h'), array('p', 'r'), 'o');

if (in_array(array('p', 'h'), $a)) {
    echo "'ph' найдено\n";
}

if (in_array(array('f', 'i'), $a)) {
    echo "'fi' найдено\n";
}

if (in_array('o', $a)) {
    echo "'o' найдено\n";
}
?>
```

Результат виконання цього прикладу:

```
'ph' найдено
  'o' найдено
```

### Дивіться також

-   [arraysearch()](function.array-search.md) - Здійснює пошук даного значення в масиві та повертає ключ першого знайденого елемента у разі успішного виконання
-   [isset()](function.isset.md) - Визначає, чи була встановлена ​​змінна значенням, відмінним від null
-   [arraykeyexists()](function.array-key-exists.md) - Перевіряє, чи присутній у масиві зазначений ключ чи індекс
