---
navigation:
  - function.str-repeat.html: « strrepeat
  - function.str-rot13.html: strrot13 »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: strreplace
---
# strreplace

(PHP 4, PHP 5, PHP 7, PHP 8)

strreplace — Замінює всі входження рядка пошуку на рядок заміни

### Опис

```methodsynopsis
str_replace(    array|string $search,    array|string $replace,    string|array $subject,    int &$count = null): string|array
```

Ця функція повертає рядок або масив, в якому всі входження `search` в `subject` замінені на `replace`

Якщо не потрібні складні правила пошуку/заміни (наприклад, регулярні вирази), використання цієї функції краще [pregreplace()](function.preg-replace.html)

### Список параметрів

Якщо `search` і `replace` - масиви, то **strreplace()** використовує кожне значення з відповідного масиву для пошуку та заміни в `subject`. Якщо в масиві `replace` менше елементів, ніж у `search`, як рядок заміни для значень, що залишилися, буде використаний порожній рядок. Якщо `search` - масив, а `replace` - рядок, то цей рядок заміни буде використаний для кожного елемента масиву `search`. Зворотний випадок не має сенсу.

Якщо `search` або `replace` є масивами, їх елементи будуть оброблені від першого до останнього.

`search`

Шукане значення, також відоме як *needle* (голка). Для безлічі значень, що шукаються, можна використовувати масив.

`replace`

Значення заміни, буде використано для заміни значень, що шукаються `search`. Для багатьох значень можна використовувати масив.

`subject`

Рядок або масив, в якому проводиться пошук і заміна, також відомий як *haystack* (Стіг сіна).

Якщо `subject` є масивом, то пошук із заміною буде здійснюватися над кожним елементом `subject`, а результатом функції також буде масив.

`count`

Якщо передано, то буде встановлено кількість проведених замін.

### Значення, що повертаються

Ця функція повертає рядок або масив із заміненими значеннями.

### Приклади

**Приклад #1 Приклади використання **strreplace()****

```php
<?php
// присваивает <body text='black'>
$bodytag = str_replace("%body%", "black", "<body text='%body%'>");

// присваивает: Hll Wrld f PHP
$vowels = array("a", "e", "i", "o", "u", "A", "E", "I", "O", "U");
$onlyconsonants = str_replace($vowels, "", "Hello World of PHP");

// присваивает: You should eat pizza, beer, and ice cream every day
$phrase  = "You should eat fruits, vegetables, and fiber every day.";
$healthy = array("fruits", "vegetables", "fiber");
$yummy   = array("pizza", "beer", "ice cream");

$newphrase = str_replace($healthy, $yummy, $phrase);

// присваивает: 2
$str = str_replace("ll", "", "good golly miss molly!", $count);
echo $count;
?>
```

**Приклад #2 Приклади потенційних трюків з **strreplace()****

```php
<?php
// Порядок замены
$str     = "Строка 1\nСтрока 2\rСтрока 3\r\nСтрока 4\n";
$order   = array("\r\n", "\n", "\r");
$replace = '<br />';

// Обрабатывает сначала \r\n для избежания их повторной замены.
echo $newstr = str_replace($order, $replace, $str);

// Выводит F, т.к. A заменяется на B, затем B на C, и так далее...
// В итоге E будет заменено F, так как замена происходит слева направо.
$search  = array('A', 'B', 'C', 'D', 'E');
$replace = array('B', 'C', 'D', 'E', 'F');
$subject = 'A';
echo str_replace($search, $replace, $subject);

// Выводит: яблорехкорех орех (по вышеуказанной причине)
$letters = array('я', 'о');
$fruit   = array('яблоко', 'орех');
$text    = 'я о';
$output  = str_replace($letters, $fruit, $text);
echo $output;
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

**Застереження**

# Зауваження щодо порядку заміни

Так як **strreplace()** здійснює заміну ліворуч, то при використанні множинних замін вона може замінити раніше вставлене значення на інше. Дивіться приклади на цій сторінці.

> **Зауваження**
> 
> Ця функція чутлива до регістру. Використовуйте [strireplace()](function.str-ireplace.html) для заміни без урахування регістру.

### Дивіться також

-   [strireplace()](function.str-ireplace.html) - Реєстронезалежний варіант функції strreplace
-   [substrreplace()](function.substr-replace.html) - Замінює частину рядка
-   [pregreplace()](function.preg-replace.html) - Виконує пошук та заміну за регулярним виразом
-   [strtr()](function.strtr.html) - Перетворює задані символи або замінює підрядки
