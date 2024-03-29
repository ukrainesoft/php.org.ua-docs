---
navigation:
  - function.strnatcasecmp.md: « strnatcasecmp
  - function.strncasecmp.md: strncasecmp »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strnatcmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strnatcmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strnatcmp - Порівняння рядків з використанням алгоритму "natural order"

### Опис

```methodsynopsis
strnatcmp(string $string1, string $string2): int
```

Ця функція реалізує алгоритм порівняння, який упорядковує алфавітно-цифрові рядки подібно до того, як це зробив би людина, такий алгоритм називається "natural ordering". Порівняння відбувається з урахуванням регістру.

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

### Значення, що повертаються

Повертає `-1`, якщо `string1`меньше`string2` , якщо `string1`больше`string2`, и якщо рядки рівні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функція тепер повертає `-1`или ; раніше вона повертала негативне чи позитивне число. |

### Приклади

Приклад, що показує відмінність цього алгоритму від звичайних функцій порівняння (використовуються в [strcmp()](function.strcmp.md)), наведений нижче:

```php
<?php
$arr1 = $arr2 = array("img12.png", "img10.png", "img2.png", "img1.png");
echo "Стандартный алгоритм сравнения\n";
usort($arr1, "strcmp");
print_r($arr1);
echo "\nАлгоритм \"natural order\"\n";
usort($arr2, "strnatcmp");
print_r($arr2);
?>
```

Результат виконання наведеного прикладу:

```
Стандартный алгоритм сравнения
Array
(
    [0] => img1.png
    [1] => img10.png
    [2] => img12.png
    [3] => img2.png
)

Алгоритм "natural order"
Array
(
    [0] => img1.png
    [1] => img2.png
    [2] => img10.png
    [3] => img12.png
)
```

Для получения дополнительной информации смотрите[» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Дивіться також

-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [strcasecmp()](function.strcasecmp.md) \- Бінарно-безпечне порівняння рядків без урахування регістру
-   [substr()](function.substr.md) \- Повертає підрядок
-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [strcmp()](function.strcmp.md) \- Бінарно-безпечне порівняння рядків
-   [strncmp()](function.strncmp.md) \- Бінарно-безпечне порівняння перших n символів рядків
-   [strncasecmp()](function.strncasecmp.md) \- Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strnatcasecmp()](function.strnatcasecmp.md) - Порівняння рядків без урахування регістру з використанням алгоритму "natural order"
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [natsort()](function.natsort.md) - Сортує масив, використовуючи алгоритм "natural order"
-   [natcasesort()](function.natcasesort.md) \- Сортує масив алгоритмом природного сортування (natural order) без урахування регістру символів
