---
navigation:
  - control-structures.foreach.md: « foreach
  - control-structures.continue.md: continue »
  - index.md: PHP Manual
  - language.control-structures.md: Керуючі конструкції
title: break
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## break

(PHP 4, PHP 5, PHP 7, PHP 8)

`break` перериває виконання поточної структури `for` `foreach` `while` `do-while`или`switch`

`break` приймає необов'язковий числовий аргумент, який повідомляє йому виконання якої кількості вкладених структур необхідно перервати. Значення за замовчуванням тільки найближча структура буде перервана.

```php
<?php
$arr = array('один', 'два', 'три', 'четыре', 'стоп', 'пять');
foreach ($arr as $val) {
    if ($val == 'стоп') {
        break;    /* Тут можно было написать 'break 1;'. */
    }
    echo "$val<br />\n";
}

/* Использование дополнительного аргумента. */

$i = 0;
while (++$i) {
    switch ($i) {
        case 5:
            echo "Итерация 5<br />\n";
            break 1;  /* Выйти только из конструкции switch. */
        case 10:
            echo "Итерация 10; выходим<br />\n";
            break 2;  /* Выходим из конструкции switch и из цикла while. */
        default:
            break;
    }
}
?>
```
