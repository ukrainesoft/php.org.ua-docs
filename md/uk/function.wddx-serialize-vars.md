---
navigation:
  - function.wddx-serialize-value.html: « wddxserializevalue
  - book.xmldiff.html: XMLDiff »
  - index.html: PHP Manual
  - ref.wddx.html: Функції WDDX
title: wddxserializevars
---
# wddxserializevars

(PHP 4, PHP 5, PHP 7)

wddxserializevars — Серіалізація змінних у пакет WDDX

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_serialize_vars(mixed $var_name, mixed ...$var_names): string
```

Створює пакет WDDX із структурою, що містить серіалізоване уявлення переданих змінних.

### Список параметрів

Функція приймає змінну кількість параметрів.

`var_name`

Може бути або рядком, що означає змінну, або масивом, що містить рядки з назвами змінних або інший масив і т.д.

`var_names`

### Значення, що повертаються

Повертає пакет WDDX або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **wddxserializevars()****

```php
<?php
$a = 1;
$b = 5.5;
$c = array("blue", "orange", "violet");
$d = "colors";

$clvars = array("c", "d");
echo wddx_serialize_vars("a", "b", $clvars);
?>
```

Результат виконання цього прикладу:

```
<wddxPacket version='1.0'><header/><data><struct><var name='a'><number>1</number></var>
<var name='b'><number>5.5</number></var><var name='c'><array length='3'>
<string>blue</string><string>orange</string><string>violet</string></array></var>
<var name='d'><string>colors</string></var></struct></data></wddxPacket>
```
