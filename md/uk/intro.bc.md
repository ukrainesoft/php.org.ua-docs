---
navigation:
  - book.bc.md: « BC Math
  - bc.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.bc.md: BC Math
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Для обчислень з довільною точністю PHP надає BCMath, який підтримує числа будь-якого розміру та точності, аж до `2147483647`(или`0x7FFFFFFF`) десяткових знаків, якщо вистачить пам'яті, поданих у вигляді рядків.

Допустимі (також відомі як правильно сформовані) числа BCMath - це рядки, що відповідають регулярному виразу `/^[+-]?[0-9]*(\.[0-9]*)?$/`

**Застереження**

Передача у функції BCMath аргументів типу float, в той час як вони очікують рядки можуть призвести до несподіваних результатів, через алгоритм PHP перетворення float в string, наприклад можна отримати рядок містить число в експоненційній нотації (який не підтримується BCMath), або, до PHP 8.0.0, залежно від локалі, десятковий роздільник у вигляді коми (тоді як BCMath працює лише з десятковою точкою).

```php
<?php
$num1 = 0; // (string) 0 => '0'
$num2 = -0.000005; // (string) -0.000005 => '-5.05E-6'
echo bcadd($num1, $num2, 6); // => '0.000000'

setlocale(LC_NUMERIC, 'de_DE'); // десятичная запятая вместо точки
$num2 = 1.2; // (string) 1.2 => '1,2'
echo bcsub($num1, $num2, 1); // => '0.0'
?>
```
